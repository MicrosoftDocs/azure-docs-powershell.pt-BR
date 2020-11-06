---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: e1a1e96dbee53dddf0731252329525620cc4933d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431912"
---
# <span data-ttu-id="8875d-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8875d-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="8875d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8875d-102">SYNOPSIS</span></span>
<span data-ttu-id="8875d-103">Move um recurso para uma assinatura ou grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="8875d-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8875d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8875d-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8875d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8875d-105">DESCRIPTION</span></span>
<span data-ttu-id="8875d-106">O cmdlet **move-AzureRmResource** move os recursos existentes para um grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="8875d-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="8875d-107">Esse grupo de recursos pode estar em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="8875d-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="8875d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8875d-108">EXAMPLES</span></span>

### <span data-ttu-id="8875d-109">Exemplo 1: mover um recurso para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8875d-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="8875d-110">O primeiro comando obtém um recurso denominado ContosoStorageAccount usando o cmdlet Get-AzureRmResource e armazena esse recurso na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="8875d-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="8875d-111">O segundo comando move o recurso para o grupo de recursos chamado ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="8875d-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="8875d-112">O comando identifica o recurso para mover usando a propriedade **ResourceId** de $Resource.</span><span class="sxs-lookup"><span data-stu-id="8875d-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="8875d-113">OS</span><span class="sxs-lookup"><span data-stu-id="8875d-113">PARAMETERS</span></span>

### <span data-ttu-id="8875d-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8875d-114">-ApiVersion</span></span>
<span data-ttu-id="8875d-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8875d-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8875d-116">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8875d-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8875d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8875d-117">-DefaultProfile</span></span>
<span data-ttu-id="8875d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8875d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8875d-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8875d-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="8875d-120">Especifica o nome do grupo de recursos no qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="8875d-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8875d-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8875d-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="8875d-122">Especifica a ID da assinatura na qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="8875d-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8875d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8875d-123">-Force</span></span>
<span data-ttu-id="8875d-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8875d-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8875d-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8875d-125">-InformationAction</span></span>
<span data-ttu-id="8875d-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="8875d-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8875d-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8875d-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8875d-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="8875d-128">Continue</span></span>
- <span data-ttu-id="8875d-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="8875d-129">Ignore</span></span>
- <span data-ttu-id="8875d-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="8875d-130">Inquire</span></span>
- <span data-ttu-id="8875d-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8875d-131">SilentlyContinue</span></span>
- <span data-ttu-id="8875d-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="8875d-132">Stop</span></span>
- <span data-ttu-id="8875d-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="8875d-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8875d-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8875d-134">-InformationVariable</span></span>
<span data-ttu-id="8875d-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="8875d-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8875d-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="8875d-136">-Pre</span></span>
<span data-ttu-id="8875d-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8875d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8875d-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8875d-138">-ResourceId</span></span>
<span data-ttu-id="8875d-139">Especifica uma matriz de IDs dos recursos que esse cmdlet Move.</span><span class="sxs-lookup"><span data-stu-id="8875d-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8875d-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8875d-140">-Confirm</span></span>
<span data-ttu-id="8875d-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8875d-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8875d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8875d-142">-WhatIf</span></span>
<span data-ttu-id="8875d-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8875d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8875d-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8875d-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8875d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8875d-145">CommonParameters</span></span>
<span data-ttu-id="8875d-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8875d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8875d-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8875d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8875d-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8875d-148">INPUTS</span></span>

## <span data-ttu-id="8875d-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8875d-149">OUTPUTS</span></span>

## <span data-ttu-id="8875d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8875d-150">NOTES</span></span>

## <span data-ttu-id="8875d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8875d-151">RELATED LINKS</span></span>

[<span data-ttu-id="8875d-152">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8875d-152">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="8875d-153">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8875d-153">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="8875d-154">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8875d-154">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="8875d-155">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8875d-155">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="8875d-156">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8875d-156">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


