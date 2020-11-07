---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 451d70b899f2cb580e23751f6662cd300c301942
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93786610"
---
# <span data-ttu-id="32a6d-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="32a6d-101">Get-AzResource</span></span>

## <span data-ttu-id="32a6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32a6d-102">SYNOPSIS</span></span>

<span data-ttu-id="32a6d-103">Obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="32a6d-103">Gets resources.</span></span>

## <span data-ttu-id="32a6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32a6d-104">SYNTAX</span></span>

### <span data-ttu-id="32a6d-105">ByTagNameValueParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="32a6d-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a6d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="32a6d-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a6d-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32a6d-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32a6d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32a6d-108">DESCRIPTION</span></span>

<span data-ttu-id="32a6d-109">O cmdlet **Get-AzResource** Obtém os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="32a6d-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="32a6d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32a6d-110">EXAMPLES</span></span>

### <span data-ttu-id="32a6d-111">Exemplo 1: obter todos os recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="32a6d-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="32a6d-112">Este comando obtém todos os recursos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="32a6d-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="32a6d-113">Exemplo 2: obter todos os recursos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="32a6d-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="32a6d-114">Esse comando obtém todos os recursos no grupo de recursos "testRG".</span><span class="sxs-lookup"><span data-stu-id="32a6d-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="32a6d-115">Exemplo 3: obter todos os recursos cujo grupo de recursos corresponde ao curinga fornecido</span><span class="sxs-lookup"><span data-stu-id="32a6d-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="32a6d-116">Esse comando obtém todos os recursos cujo grupo de recursos ele pertence a usuários com "outros".</span><span class="sxs-lookup"><span data-stu-id="32a6d-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="32a6d-117">Exemplo 4: obter todos os recursos com um nome específico</span><span class="sxs-lookup"><span data-stu-id="32a6d-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="32a6d-118">Esse comando obtém todos os recursos cujo nome do recurso é "testVM".</span><span class="sxs-lookup"><span data-stu-id="32a6d-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="32a6d-119">Exemplo 5: obter todos os recursos cujo nome corresponde ao curinga fornecido</span><span class="sxs-lookup"><span data-stu-id="32a6d-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="32a6d-120">Esse comando obtém todos os recursos cujo nome do recurso começa com "Test".</span><span class="sxs-lookup"><span data-stu-id="32a6d-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="32a6d-121">Exemplo 6: obter todos os recursos de um determinado tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="32a6d-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="32a6d-122">Esse comando obtém todos os recursos nas assinaturas atuais que são máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="32a6d-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="32a6d-123">Exemplo 7: obter um recurso por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="32a6d-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="32a6d-124">Esse comando obtém o recurso com a ID de recurso fornecida, que é uma máquina virtual chamada "testVM" no grupo de recursos "testRG".</span><span class="sxs-lookup"><span data-stu-id="32a6d-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="32a6d-125">OS</span><span class="sxs-lookup"><span data-stu-id="32a6d-125">PARAMETERS</span></span>

### <span data-ttu-id="32a6d-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="32a6d-126">-ApiVersion</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a6d-127">-DefaultProfile</span></span>
<span data-ttu-id="32a6d-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="32a6d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-129">-Expandproperties</span><span class="sxs-lookup"><span data-stu-id="32a6d-129">-ExpandProperties</span></span>
<span data-ttu-id="32a6d-130">Quando especificado, expande as propriedades do recurso.</span><span class="sxs-lookup"><span data-stu-id="32a6d-130">When specified, expands the properties of the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="32a6d-131">-Name</span></span>
<span data-ttu-id="32a6d-132">O nome do (s) recurso (s) a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="32a6d-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="32a6d-133">Esse parâmetro dá suporte a caracteres curinga no início e/ou final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="32a6d-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="32a6d-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="32a6d-134">-ODataQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="32a6d-135">-Pre</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a6d-136">-ResourceGroupName</span></span>
<span data-ttu-id="32a6d-137">O grupo de recursos ao qual o (s) recurso (s) recuperado (s) pertence.</span><span class="sxs-lookup"><span data-stu-id="32a6d-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="32a6d-138">Esse parâmetro dá suporte a caracteres curinga no início e/ou final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="32a6d-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="32a6d-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32a6d-139">-ResourceId</span></span>
<span data-ttu-id="32a6d-140">Especifica a ID de recurso totalmente qualificado, como no exemplo a seguir `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="32a6d-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="32a6d-141">-ResourceType</span></span>
<span data-ttu-id="32a6d-142">O tipo de recurso do (s) recurso (s) a ser recuperado (s).</span><span class="sxs-lookup"><span data-stu-id="32a6d-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="32a6d-143">Por exemplo, Microsoft. Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="32a6d-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="32a6d-144">-Tag</span></span>

<span data-ttu-id="32a6d-145">Obtém recursos que têm a marca do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="32a6d-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="32a6d-146">Insira uma tabela de hash com uma chave de nome ou um nome e as teclas de valor.</span><span class="sxs-lookup"><span data-stu-id="32a6d-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="32a6d-147">Não há suporte para caracteres curinga. Uma "marca" é um par de nome-valor que você pode aplicar a recursos e grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="32a6d-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="32a6d-148">Use marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para controlar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="32a6d-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="32a6d-149">Para adicionar uma marca a um recurso, use o parâmetro Tag dos cmdlets New-AzResource ou Set-AzResource.</span><span class="sxs-lookup"><span data-stu-id="32a6d-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="32a6d-150">Para criar uma marca predefinida, use o cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="32a6d-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="32a6d-151">Para obter ajuda com tabelas de hash no Windows PowerShell, execute ' Get-Help about_Hashtables '.</span><span class="sxs-lookup"><span data-stu-id="32a6d-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="32a6d-152">-TagName</span></span>
<span data-ttu-id="32a6d-153">A chave na marca do (s) recurso (s) a ser recuperada (s).</span><span class="sxs-lookup"><span data-stu-id="32a6d-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="32a6d-154">-TagValue</span></span>
<span data-ttu-id="32a6d-155">O valor na marca do (s) recurso (s) a ser recuperado (s).</span><span class="sxs-lookup"><span data-stu-id="32a6d-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a6d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a6d-156">CommonParameters</span></span>
<span data-ttu-id="32a6d-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a6d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a6d-158">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32a6d-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a6d-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32a6d-159">INPUTS</span></span>

### <span data-ttu-id="32a6d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="32a6d-160">System.String</span></span>

## <span data-ttu-id="32a6d-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32a6d-161">OUTPUTS</span></span>

### <span data-ttu-id="32a6d-162">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="32a6d-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="32a6d-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32a6d-163">NOTES</span></span>

## <span data-ttu-id="32a6d-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32a6d-164">RELATED LINKS</span></span>

[<span data-ttu-id="32a6d-165">Mover-AzResource</span><span class="sxs-lookup"><span data-stu-id="32a6d-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="32a6d-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="32a6d-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="32a6d-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="32a6d-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="32a6d-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="32a6d-168">Set-AzResource</span></span>](./Set-AzResource.md)
