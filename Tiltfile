k8s_yaml('config.yaml')
k8s_yaml('config2.yaml')

deps = listdir('src')[:4000]

custom_build(
  'test',
  'docker build -t $EXPECTED_REF src',
  deps=listdir('src')[:4000],
)

custom_build(
  'test2',
  'docker build -t $EXPECTED_REF src2',
  deps=listdir('src2')[:4000],
)