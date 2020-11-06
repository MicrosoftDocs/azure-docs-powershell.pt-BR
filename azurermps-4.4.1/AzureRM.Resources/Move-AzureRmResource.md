---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4a40b3fd0045a48d6a69c76970b3835ef2d685c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603329"
---
# <span data-ttu-id="9e24c-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e24c-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="9e24c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e24c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e24c-103">Move um recurso para uma assinatura ou grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="9e24c-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e24c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e24c-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e24c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e24c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e24c-106">O cmdlet **move-AzureRmResource** move os recursos existentes para um grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="9e24c-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="9e24c-107">Esse grupo de recursos pode estar em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="9e24c-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="9e24c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e24c-108">EXAMPLES</span></span>

### <span data-ttu-id="9e24c-109">Exemplo 1: mover um recurso para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9e24c-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="9e24c-110">O primeiro comando obtém um recurso denominado ContosoStorageAccount usando o cmdlet Get-AzureRmResource e armazena esse recurso na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="9e24c-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="9e24c-111">O segundo comando move o recurso para o grupo de recursos chamado ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="9e24c-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="9e24c-112">O comando identifica o recurso para mover usando a propriedade **ResourceId** de $Resource.</span><span class="sxs-lookup"><span data-stu-id="9e24c-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="9e24c-113">OS</span><span class="sxs-lookup"><span data-stu-id="9e24c-113">PARAMETERS</span></span>

### <span data-ttu-id="9e24c-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9e24c-114">-ApiVersion</span></span>
<span data-ttu-id="9e24c-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9e24c-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9e24c-116">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="9e24c-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9e24c-117">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e24c-117">-DestinationResourceGroupName</span></span>
<span data-ttu-id="9e24c-118">Especifica o nome do grupo de recursos no qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="9e24c-118">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="9e24c-119">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e24c-119">-DestinationSubscriptionId</span></span>
<span data-ttu-id="9e24c-120">Especifica a ID da assinatura na qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="9e24c-120">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="9e24c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9e24c-121">-Force</span></span>
<span data-ttu-id="9e24c-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9e24c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e24c-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9e24c-123">-InformationAction</span></span>
<span data-ttu-id="9e24c-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9e24c-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9e24c-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e24c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e24c-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9e24c-126">Continue</span></span>
- <span data-ttu-id="9e24c-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9e24c-127">Ignore</span></span>
- <span data-ttu-id="9e24c-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="9e24c-128">Inquire</span></span>
- <span data-ttu-id="9e24c-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9e24c-129">SilentlyContinue</span></span>
- <span data-ttu-id="9e24c-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9e24c-130">Stop</span></span>
- <span data-ttu-id="9e24c-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9e24c-131">Suspend</span></span>

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

### <span data-ttu-id="9e24c-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9e24c-132">-InformationVariable</span></span>
<span data-ttu-id="9e24c-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9e24c-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9e24c-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="9e24c-134">-Pre</span></span>
<span data-ttu-id="9e24c-135">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9e24c-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9e24c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e24c-136">-ResourceId</span></span>
<span data-ttu-id="9e24c-137">Especifica uma matriz de IDs dos recursos que esse cmdlet Move.</span><span class="sxs-lookup"><span data-stu-id="9e24c-137">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="9e24c-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e24c-138">-Confirm</span></span>
<span data-ttu-id="9e24c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e24c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e24c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e24c-140">-WhatIf</span></span>
<span data-ttu-id="9e24c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e24c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e24c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e24c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e24c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e24c-143">-DefaultProfile</span></span>
<span data-ttu-id="9e24c-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e24c-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e24c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e24c-145">CommonParameters</span></span>
<span data-ttu-id="9e24c-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e24c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e24c-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e24c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e24c-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e24c-148">INPUTS</span></span>

### <span data-ttu-id="9e24c-149">String []</span><span class="sxs-lookup"><span data-stu-id="9e24c-149">String[]</span></span>
<span data-ttu-id="9e24c-150">O parâmetro ' ResourceId ' aceita o valor do tipo ' String [] ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9e24c-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="9e24c-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e24c-151">OUTPUTS</span></span>

### <span data-ttu-id="9e24c-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e24c-152">System.Boolean</span></span>

## <span data-ttu-id="9e24c-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e24c-153">NOTES</span></span>

## <span data-ttu-id="9e24c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e24c-154">RELATED LINKS</span></span>

[<span data-ttu-id="9e24c-155">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e24c-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="9e24c-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e24c-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="9e24c-157">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e24c-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="9e24c-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e24c-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="9e24c-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e24c-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


