---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603333"
---
# <span data-ttu-id="769eb-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="769eb-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="769eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="769eb-102">SYNOPSIS</span></span>
<span data-ttu-id="769eb-103">Obtém grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="769eb-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="769eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="769eb-104">SYNTAX</span></span>

### <span data-ttu-id="769eb-105">Lista o grupo de recursos com base no nome.</span><span class="sxs-lookup"><span data-stu-id="769eb-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="769eb-106">Assume</span><span class="sxs-lookup"><span data-stu-id="769eb-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="769eb-107">Lista o grupo de recursos com base na ID.</span><span class="sxs-lookup"><span data-stu-id="769eb-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="769eb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="769eb-108">DESCRIPTION</span></span>
<span data-ttu-id="769eb-109">O cmdlet **Get-AzureRmResourceGroup** Obtém grupos de recursos do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="769eb-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="769eb-110">Você pode obter todos os grupos de recursos ou especificar um grupo de recursos por nome ou por outras propriedades.</span><span class="sxs-lookup"><span data-stu-id="769eb-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="769eb-111">Por padrão, esse cmdlet obtém todos os grupos de recursos na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="769eb-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="769eb-112">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="769eb-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="769eb-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="769eb-113">EXAMPLES</span></span>

### <span data-ttu-id="769eb-114">Exemplo 1: obter um grupo de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="769eb-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="769eb-115">Esse comando obtém o grupo de recursos do Azure na sua assinatura chamado EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="769eb-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="769eb-116">Exemplo 2: obter todas as marcas de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="769eb-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="769eb-117">Esse comando obtém o grupo de recursos denominado ContosoRG e exibe as marcas associadas a esse grupo.</span><span class="sxs-lookup"><span data-stu-id="769eb-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="769eb-118">OS</span><span class="sxs-lookup"><span data-stu-id="769eb-118">PARAMETERS</span></span>

### <span data-ttu-id="769eb-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="769eb-119">-ApiVersion</span></span>
<span data-ttu-id="769eb-120">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="769eb-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="769eb-121">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="769eb-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="769eb-122">-ID</span><span class="sxs-lookup"><span data-stu-id="769eb-122">-Id</span></span>
<span data-ttu-id="769eb-123">Especifica a ID do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="769eb-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="769eb-124">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="769eb-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769eb-125">-Local</span><span class="sxs-lookup"><span data-stu-id="769eb-125">-Location</span></span>
<span data-ttu-id="769eb-126">Especifica o local do grupo de recursos a obter.</span><span class="sxs-lookup"><span data-stu-id="769eb-126">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769eb-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="769eb-127">-Name</span></span>
<span data-ttu-id="769eb-128">Especifica o nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="769eb-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="769eb-129">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="769eb-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="769eb-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="769eb-130">-Pre</span></span>
<span data-ttu-id="769eb-131">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="769eb-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="769eb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769eb-132">-DefaultProfile</span></span>
<span data-ttu-id="769eb-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="769eb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="769eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769eb-134">CommonParameters</span></span>
<span data-ttu-id="769eb-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769eb-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="769eb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769eb-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="769eb-137">INPUTS</span></span>

### <span data-ttu-id="769eb-138">String</span><span class="sxs-lookup"><span data-stu-id="769eb-138">String</span></span>
<span data-ttu-id="769eb-139">Você pode canalizar a entrada para o cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="769eb-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="769eb-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="769eb-140">OUTPUTS</span></span>

### <span data-ttu-id="769eb-141">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="769eb-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="769eb-142">Esse cmdlet retorna grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="769eb-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="769eb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="769eb-143">NOTES</span></span>

## <span data-ttu-id="769eb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="769eb-144">RELATED LINKS</span></span>

[<span data-ttu-id="769eb-145">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="769eb-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="769eb-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="769eb-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="769eb-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="769eb-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


