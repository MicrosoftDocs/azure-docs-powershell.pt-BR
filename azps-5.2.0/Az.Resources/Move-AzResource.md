---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d14d591ffdc0e20934a0cf758407dc2b4e6e152c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256577"
---
# <span data-ttu-id="27762-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="27762-101">Move-AzResource</span></span>

## <span data-ttu-id="27762-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27762-102">SYNOPSIS</span></span>
<span data-ttu-id="27762-103">Move um recurso para uma assinatura ou grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="27762-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="27762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27762-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27762-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27762-105">DESCRIPTION</span></span>
<span data-ttu-id="27762-106">O cmdlet **move-AzResource** move os recursos existentes para um grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="27762-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="27762-107">Esse grupo de recursos pode estar em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="27762-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="27762-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27762-108">EXAMPLES</span></span>

### <span data-ttu-id="27762-109">Exemplo 1: mover um recurso para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="27762-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="27762-110">O primeiro comando obtém um recurso denominado ContosoStorageAccount usando o cmdlet Get-AzResource e armazena esse recurso na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="27762-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="27762-111">O segundo comando move o recurso para o grupo de recursos chamado ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="27762-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="27762-112">O comando identifica o recurso para mover usando a propriedade **ResourceId** de $Resource.</span><span class="sxs-lookup"><span data-stu-id="27762-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="27762-113">OS</span><span class="sxs-lookup"><span data-stu-id="27762-113">PARAMETERS</span></span>

### <span data-ttu-id="27762-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="27762-114">-ApiVersion</span></span>
<span data-ttu-id="27762-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="27762-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="27762-116">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="27762-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="27762-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27762-117">-DefaultProfile</span></span>
<span data-ttu-id="27762-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="27762-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27762-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27762-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="27762-120">Especifica o nome do grupo de recursos no qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="27762-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="27762-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27762-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="27762-122">Especifica a ID da assinatura na qual esse cmdlet Move recursos.</span><span class="sxs-lookup"><span data-stu-id="27762-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="27762-123">-Force</span><span class="sxs-lookup"><span data-stu-id="27762-123">-Force</span></span>
<span data-ttu-id="27762-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="27762-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27762-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="27762-125">-Pre</span></span>
<span data-ttu-id="27762-126">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="27762-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="27762-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27762-127">-ResourceId</span></span>
<span data-ttu-id="27762-128">Especifica uma matriz de IDs dos recursos que esse cmdlet Move.</span><span class="sxs-lookup"><span data-stu-id="27762-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="27762-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27762-129">-Confirm</span></span>
<span data-ttu-id="27762-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27762-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27762-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27762-131">-WhatIf</span></span>
<span data-ttu-id="27762-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27762-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27762-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27762-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27762-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27762-134">CommonParameters</span></span>
<span data-ttu-id="27762-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27762-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27762-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27762-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27762-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27762-137">INPUTS</span></span>

### <span data-ttu-id="27762-138">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="27762-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="27762-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="27762-139">System.String[]</span></span>

## <span data-ttu-id="27762-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27762-140">OUTPUTS</span></span>

### <span data-ttu-id="27762-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27762-141">System.Boolean</span></span>

## <span data-ttu-id="27762-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27762-142">NOTES</span></span>

## <span data-ttu-id="27762-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27762-143">RELATED LINKS</span></span>

[<span data-ttu-id="27762-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="27762-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="27762-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="27762-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="27762-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="27762-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="27762-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="27762-147">Set-AzResource</span></span>](./Set-AzResource.md)


