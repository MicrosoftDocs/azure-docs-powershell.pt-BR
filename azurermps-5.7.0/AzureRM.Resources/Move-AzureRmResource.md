---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4562c217a771f53995a531a3ca72066da672a144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432410"
---
# <span data-ttu-id="0d252-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d252-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="0d252-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d252-102">SYNOPSIS</span></span>
<span data-ttu-id="0d252-103">Move um recurso para uma assinatura ou grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="0d252-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d252-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d252-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d252-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d252-105">DESCRIPTION</span></span>
<span data-ttu-id="0d252-106">O cmdlet **move-AzureRmResource** move os recursos existentes para um grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="0d252-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="0d252-107">Esse grupo de recursos pode estar em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="0d252-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="0d252-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d252-108">EXAMPLES</span></span>

### <span data-ttu-id="0d252-109">Exemplo 1: mover um recurso para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0d252-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="0d252-110">O primeiro comando obtém um recurso denominado ContosoStorageAccount usando o cmdlet Get-AzureRmResource e armazena esse recurso na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="0d252-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="0d252-111">O segundo comando move o recurso para o grupo de recursos chamado ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="0d252-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="0d252-112">O comando identifica o recurso para mover usando a propriedade **ResourceId** de $Resource.</span><span class="sxs-lookup"><span data-stu-id="0d252-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="0d252-113">OS</span><span class="sxs-lookup"><span data-stu-id="0d252-113">PARAMETERS</span></span>

### <span data-ttu-id="0d252-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d252-114">-ApiVersion</span></span>
<span data-ttu-id="0d252-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0d252-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0d252-116">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="0d252-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d252-117">-DefaultProfile</span></span>
<span data-ttu-id="0d252-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0d252-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d252-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="0d252-120">Especifica o nome do grupo de recursos no qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="0d252-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d252-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="0d252-122">Especifica a ID da assinatura na qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="0d252-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0d252-123">-Force</span></span>
<span data-ttu-id="0d252-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d252-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0d252-125">-InformationAction</span></span>
<span data-ttu-id="0d252-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="0d252-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0d252-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0d252-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d252-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="0d252-128">Continue</span></span>
- <span data-ttu-id="0d252-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="0d252-129">Ignore</span></span>
- <span data-ttu-id="0d252-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="0d252-130">Inquire</span></span>
- <span data-ttu-id="0d252-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0d252-131">SilentlyContinue</span></span>
- <span data-ttu-id="0d252-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="0d252-132">Stop</span></span>
- <span data-ttu-id="0d252-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="0d252-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0d252-134">-InformationVariable</span></span>
<span data-ttu-id="0d252-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="0d252-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d252-136">-Pre</span></span>
<span data-ttu-id="0d252-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0d252-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d252-138">-ResourceId</span></span>
<span data-ttu-id="0d252-139">Especifica uma matriz de IDs dos recursos que esse cmdlet Move.</span><span class="sxs-lookup"><span data-stu-id="0d252-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0d252-140">-Confirm</span></span>
<span data-ttu-id="0d252-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d252-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d252-142">-WhatIf</span></span>
<span data-ttu-id="0d252-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d252-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d252-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d252-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d252-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d252-145">CommonParameters</span></span>
<span data-ttu-id="0d252-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d252-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d252-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d252-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d252-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d252-148">INPUTS</span></span>

### <span data-ttu-id="0d252-149">String []</span><span class="sxs-lookup"><span data-stu-id="0d252-149">String[]</span></span>
<span data-ttu-id="0d252-150">O parâmetro ' ResourceId ' aceita o valor do tipo ' String [] ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0d252-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="0d252-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d252-151">OUTPUTS</span></span>

### <span data-ttu-id="0d252-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d252-152">System.Boolean</span></span>

## <span data-ttu-id="0d252-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d252-153">NOTES</span></span>

## <span data-ttu-id="0d252-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d252-154">RELATED LINKS</span></span>

[<span data-ttu-id="0d252-155">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d252-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="0d252-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d252-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="0d252-157">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d252-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="0d252-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d252-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="0d252-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d252-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


