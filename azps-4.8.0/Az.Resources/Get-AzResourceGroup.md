---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: b8e74a0c349ea058d05ef044648e836fddc1f7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111946"
---
# <span data-ttu-id="6b534-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b534-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="6b534-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b534-102">SYNOPSIS</span></span>
<span data-ttu-id="6b534-103">Obtém grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b534-103">Gets resource groups.</span></span>

## <span data-ttu-id="6b534-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b534-104">SYNTAX</span></span>

### <span data-ttu-id="6b534-105">GetByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b534-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b534-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6b534-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b534-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b534-107">DESCRIPTION</span></span>
<span data-ttu-id="6b534-108">O cmdlet **Get-AzResourceGroup** Obtém grupos de recursos do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6b534-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="6b534-109">Você pode obter todos os grupos de recursos ou especificar um grupo de recursos por nome ou por outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="6b534-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="6b534-110">Por padrão, esse cmdlet obtém todos os grupos de recursos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6b534-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="6b534-111">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6b534-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="6b534-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b534-112">EXAMPLES</span></span>

### <span data-ttu-id="6b534-113">Exemplo 1: obter um grupo de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="6b534-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="6b534-114">Esse comando obtém o grupo de recursos do Azure na sua assinatura chamado EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="6b534-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="6b534-115">Exemplo 2: obter todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6b534-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="6b534-116">Esse comando obtém o grupo de recursos denominado ContosoRG e exibe as marcas associadas a esse grupo.</span><span class="sxs-lookup"><span data-stu-id="6b534-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="6b534-117">Exemplo 3: obter grupos de recursos com base na marca</span><span class="sxs-lookup"><span data-stu-id="6b534-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="6b534-118">Exemplo 4: mostrar os grupos de recursos por localização</span><span class="sxs-lookup"><span data-stu-id="6b534-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="6b534-119">Exemplo 5: mostrar os nomes de todos os grupos de recursos em um local específico</span><span class="sxs-lookup"><span data-stu-id="6b534-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="6b534-120">Exemplo 6: mostrar os grupos de recursos cujos nomes começam com o WebServer</span><span class="sxs-lookup"><span data-stu-id="6b534-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="6b534-121">OS</span><span class="sxs-lookup"><span data-stu-id="6b534-121">PARAMETERS</span></span>

### <span data-ttu-id="6b534-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b534-122">-ApiVersion</span></span>
<span data-ttu-id="6b534-123">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b534-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6b534-124">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="6b534-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6b534-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b534-125">-DefaultProfile</span></span>
<span data-ttu-id="6b534-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6b534-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b534-127">-ID</span><span class="sxs-lookup"><span data-stu-id="6b534-127">-Id</span></span>
<span data-ttu-id="6b534-128">Especifica a ID do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="6b534-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="6b534-129">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6b534-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b534-130">-Local</span><span class="sxs-lookup"><span data-stu-id="6b534-130">-Location</span></span>
<span data-ttu-id="6b534-131">Especifica o local do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="6b534-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b534-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b534-132">-Name</span></span>
<span data-ttu-id="6b534-133">Especifica o nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="6b534-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="6b534-134">Esse parâmetro dá suporte a caracteres curinga no início e/ou final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b534-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6b534-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b534-135">-Pre</span></span>
<span data-ttu-id="6b534-136">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6b534-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6b534-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="6b534-137">-Tag</span></span>
<span data-ttu-id="6b534-138">A Hashtable de marca para filtrar grupos de recursos por.</span><span class="sxs-lookup"><span data-stu-id="6b534-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b534-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b534-139">CommonParameters</span></span>
<span data-ttu-id="6b534-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b534-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b534-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b534-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b534-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b534-142">INPUTS</span></span>

### <span data-ttu-id="6b534-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6b534-143">System.String</span></span>

### <span data-ttu-id="6b534-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6b534-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6b534-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b534-145">OUTPUTS</span></span>

### <span data-ttu-id="6b534-146">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b534-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="6b534-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b534-147">NOTES</span></span>

## <span data-ttu-id="6b534-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b534-148">RELATED LINKS</span></span>

[<span data-ttu-id="6b534-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b534-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="6b534-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b534-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="6b534-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b534-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


