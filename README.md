# issue29108
files for issue 29108
		torch::serialize::OutputArchive output_archive;
		auto presavedModule = torch::jit::load("D:/localshare/data/model/model.pt");
		presavedModule.save("D:/localshare/data/model/testmodel.pt");
		auto savedModule = torch::jit::load("D:/localshare/data/model/testmodel.pt");
		savedModule.dump(true, true, true);
reported error:
Caught
expected newline but found 'number' here:
at code/__torch__/modelv2.py:75:51
import __torch__.modelv2.features.16.conv.1
import __torch__.modelv2.features.17
import __torch__.modelv2.features.17.conv
import __torch__.modelv2.features.17.conv.0
import __torch__.modelv2.features.17.conv.1
import __torch__.modelv2.features.18
class features(Module):
  __parameters__ = []
  __annotations__ = []
  __annotations__["0"] = __torch__.modelv2.features.0
                                                   ~~ <--- HERE
  __annotations__["1"] = __torch__.modelv2.features.1
  __annotations__["2"] = __torch__.modelv2.features.2
  __annotations__["3"] = __torch__.modelv2.features.3
  __annotations__["4"] = __torch__.modelv2.features.4
  __annotations__["5"] = __torch__.modelv2.features.5
  __annotations__["6"] = __torch__.modelv2.features.6
  __annotations__["7"] = __torch__.modelv2.features.7
  __annotations__["8"] = __torch__.modelv2.features.8
  __annotations__["9"] = __torch__.modelv2.features.9
Compiled from code
Type class std::runtime_error
