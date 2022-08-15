# code to carousel 

### function

      List<Widget> generateImageTiles(screenSize) {
          return images
             .map(
              (element) => ClipRRect(
                borderRadius: BorderRadius.circular(8.0),
                 child: Image.asset(
                   element,
               fit: BoxFit.cover,
             ),
          ),
        )
       .toList();
    }

       CarouselSlider(
        items: imageSliders,
        options: CarouselOptions(
            enlargeCenterPage: true,
            aspectRatio: 18 / 8,
            autoPlay: true,
            onPageChanged: (index, reason) {
              setState(() {
                _current = index;
              });
            }),
        carouselController: _controller,
      ),
