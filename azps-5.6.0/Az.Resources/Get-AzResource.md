---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 92a9e1820af2e850af6c3abaca71a7be1f15ed5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885260"
---
# <span data-ttu-id="aaaf9-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="aaaf9-101">Get-AzResource</span></span>

## <span data-ttu-id="aaaf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaaf9-102">SYNOPSIS</span></span>

<span data-ttu-id="aaaf9-103">Obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-103">Gets resources.</span></span>

## <span data-ttu-id="aaaf9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aaaf9-104">SYNTAX</span></span>

### <span data-ttu-id="aaaf9-105">ByTagNameValueParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aaaf9-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaaf9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aaaf9-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaaf9-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaaf9-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaaf9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aaaf9-108">DESCRIPTION</span></span>

<span data-ttu-id="aaaf9-109">O cmdlet **Get-AzResource** obtém recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="aaaf9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aaaf9-110">EXAMPLES</span></span>

### <span data-ttu-id="aaaf9-111">Exemplo 1: Obter todos os recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="aaaf9-111">Example 1: Get all resources in the current subscription</span></span>

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

<span data-ttu-id="aaaf9-112">Este comando obtém todos os recursos da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="aaaf9-113">Exemplo 2: Obter todos os recursos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="aaaf9-113">Example 2: Get all resources in a resource group</span></span>

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

<span data-ttu-id="aaaf9-114">Este comando obtém todos os recursos no grupo de recursos "testRG".</span><span class="sxs-lookup"><span data-stu-id="aaaf9-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="aaaf9-115">Exemplo 3: Obter todos os recursos cujo grupo de recursos corresponde ao caractere curinga fornecido</span><span class="sxs-lookup"><span data-stu-id="aaaf9-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="aaaf9-116">Este comando obtém todos os recursos cujo grupo de recursos pertencem a seres com "outros".</span><span class="sxs-lookup"><span data-stu-id="aaaf9-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="aaaf9-117">Exemplo 4: Obter todos os recursos com um determinado nome</span><span class="sxs-lookup"><span data-stu-id="aaaf9-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="aaaf9-118">Este comando obtém todos os recursos cujo nome do recurso é "testVM".</span><span class="sxs-lookup"><span data-stu-id="aaaf9-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="aaaf9-119">Exemplo 5: Obter todos os recursos cujo nome corresponde ao curinga fornecido</span><span class="sxs-lookup"><span data-stu-id="aaaf9-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="aaaf9-120">Este comando obtém todos os recursos cujo nome do recurso começa com "test".</span><span class="sxs-lookup"><span data-stu-id="aaaf9-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="aaaf9-121">Exemplo 6: Obter todos os recursos de um determinado tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="aaaf9-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="aaaf9-122">Esse comando obtém todos os recursos nas assinaturas atuais que são máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="aaaf9-123">Exemplo 7: Obter um recurso por id de recurso</span><span class="sxs-lookup"><span data-stu-id="aaaf9-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="aaaf9-124">Esse comando obtém o recurso com a id de recurso fornecida, que é uma máquina virtual chamada "testVM" no grupo de recursos "testRG".</span><span class="sxs-lookup"><span data-stu-id="aaaf9-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="aaaf9-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aaaf9-125">PARAMETERS</span></span>

### <span data-ttu-id="aaaf9-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aaaf9-126">-ApiVersion</span></span>

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

### <span data-ttu-id="aaaf9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaaf9-127">-DefaultProfile</span></span>
<span data-ttu-id="aaaf9-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aaaf9-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaaf9-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="aaaf9-129">-ExpandProperties</span></span>
<span data-ttu-id="aaaf9-130">Quando especificado, expande as propriedades do recurso.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="aaaf9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="aaaf9-131">-Name</span></span>
<span data-ttu-id="aaaf9-132">O nome dos recursos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="aaaf9-133">Este parâmetro dá suporte a caracteres curinga no início e/ou fim da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="aaaf9-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="aaaf9-134">-ODataQuery</span></span>

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

### <span data-ttu-id="aaaf9-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="aaaf9-135">-Pre</span></span>

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

### <span data-ttu-id="aaaf9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaaf9-136">-ResourceGroupName</span></span>
<span data-ttu-id="aaaf9-137">O grupo de recursos do(s) recurso (s) que é recuperado pertence.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="aaaf9-138">Este parâmetro dá suporte a caracteres curinga no início e/ou fim da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="aaaf9-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaaf9-139">-ResourceId</span></span>
<span data-ttu-id="aaaf9-140">Especifica a ID de recurso totalmente qualificada, como no exemplo a seguir `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="aaaf9-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="aaaf9-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aaaf9-141">-ResourceType</span></span>
<span data-ttu-id="aaaf9-142">O tipo de recurso dos recursos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="aaaf9-143">Por exemplo, Microsoft.Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="aaaf9-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="aaaf9-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="aaaf9-144">-Tag</span></span>

<span data-ttu-id="aaaf9-145">Obtém recursos que têm a marca do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="aaaf9-146">Insira uma tabela de hash com uma chave Name ou teclas Name e Value.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="aaaf9-147">Caracteres curinga não são suportados. Uma "marca" é um par de valores de nome que você pode aplicar a recursos e grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="aaaf9-148">Use marcas para categorizar seus recursos, como por departamento ou centro de custo, ou para acompanhar anotações ou comentários sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="aaaf9-149">Para adicionar uma marca a um recurso, use o parâmetro Tag do New-AzResource ou Set-AzResource cmdlets.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="aaaf9-150">Para criar uma marca predefinida, use New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="aaaf9-151">Para obter ajuda com tabelas de hash Windows PowerShell, execute 'Get-Help about_Hashtables'.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="aaaf9-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="aaaf9-152">-TagName</span></span>
<span data-ttu-id="aaaf9-153">A chave na marca dos recursos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="aaaf9-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="aaaf9-154">-TagValue</span></span>
<span data-ttu-id="aaaf9-155">O valor na marca dos recursos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="aaaf9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaaf9-156">CommonParameters</span></span>
<span data-ttu-id="aaaf9-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaaf9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaaf9-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaaf9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaaf9-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaaf9-159">INPUTS</span></span>

### <span data-ttu-id="aaaf9-160">System.String</span><span class="sxs-lookup"><span data-stu-id="aaaf9-160">System.String</span></span>

## <span data-ttu-id="aaaf9-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aaaf9-161">OUTPUTS</span></span>

### <span data-ttu-id="aaaf9-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="aaaf9-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="aaaf9-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="aaaf9-163">NOTES</span></span>

## <span data-ttu-id="aaaf9-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaaf9-164">RELATED LINKS</span></span>

[<span data-ttu-id="aaaf9-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="aaaf9-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="aaaf9-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="aaaf9-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="aaaf9-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="aaaf9-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="aaaf9-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="aaaf9-168">Set-AzResource</span></span>](./Set-AzResource.md)