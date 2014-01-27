set(P3GRUTIL_HEADERS
  pipeOcclusionCullTraverser.I pipeOcclusionCullTraverser.h
  cardMaker.I cardMaker.h
  config_grutil.h
  movieTexture.I movieTexture.h
  fisheyeMaker.I fisheyeMaker.h
  frameRateMeter.I frameRateMeter.h
  meshDrawer.I meshDrawer.h
  meshDrawer2D.I meshDrawer2D.h
  geoMipTerrain.I geoMipTerrain.h
  sceneGraphAnalyzerMeter.I sceneGraphAnalyzerMeter.h
  heightfieldTesselator.I heightfieldTesselator.h
  lineSegs.I lineSegs.h
  multitexReducer.I multitexReducer.h
  nodeVertexTransform.I nodeVertexTransform.h
  pfmVizzer.I pfmVizzer.h
  rigidBodyCombiner.I rigidBodyCombiner.h
)
set(P3GRUTIL_SOURCES
  cardMaker.cxx
  movieTexture.cxx
  fisheyeMaker.cxx
  config_grutil.cxx
  frameRateMeter.cxx
  meshDrawer.cxx
  meshDrawer2D.cxx
  geoMipTerrain.cxx
  sceneGraphAnalyzerMeter.cxx
  heightfieldTesselator.cxx
  nodeVertexTransform.cxx
  pfmVizzer.cxx
  pipeOcclusionCullTraverser.cxx
  lineSegs.cxx
  rigidBodyCombiner.cxx
)

composite_sources(p3grutil P3GRUTIL_SOURCES)
add_library(p3grutil ${P3GRUTIL_SOURCES} ${P3GRUTIL_HEADERS})
target_link_libraries(p3grutil p3display p3text)
target_interrogate(p3grutil ALL)