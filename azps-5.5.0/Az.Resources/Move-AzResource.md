---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d14d591ffdc0e20934a0cf758407dc2b4e6e152c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114905"
---
# <span data-ttu-id="ec09b-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="ec09b-101">Move-AzResource</span></span>

## <span data-ttu-id="ec09b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec09b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec09b-103">Move um recurso para um grupo de recursos ou assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="ec09b-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="ec09b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec09b-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec09b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec09b-105">DESCRIPTION</span></span>
<span data-ttu-id="ec09b-106">O **cmdlet Move-AzResource** move os recursos existentes para um grupo de recursos diferente.</span><span class="sxs-lookup"><span data-stu-id="ec09b-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="ec09b-107">Esse grupo de recursos pode estar em uma assinatura diferente.</span><span class="sxs-lookup"><span data-stu-id="ec09b-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="ec09b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ec09b-108">EXAMPLES</span></span>

### <span data-ttu-id="ec09b-109">Exemplo 1: Mover um recurso para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ec09b-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="ec09b-110">O primeiro comando obtém um recurso chamado ContosoStorageAccount usando o cmdlet Get-AzResource e armazena esse recurso na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="ec09b-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="ec09b-111">O segundo comando move esse recurso para o grupo de recursos chamado ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="ec09b-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="ec09b-112">O comando identifica o recurso a ser movimentado usando a propriedade **ResourceId** do $Resource.</span><span class="sxs-lookup"><span data-stu-id="ec09b-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="ec09b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec09b-113">PARAMETERS</span></span>

### <span data-ttu-id="ec09b-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ec09b-114">-ApiVersion</span></span>
<span data-ttu-id="ec09b-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ec09b-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ec09b-116">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="ec09b-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ec09b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec09b-117">-DefaultProfile</span></span>
<span data-ttu-id="ec09b-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ec09b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec09b-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec09b-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="ec09b-120">Especifica o nome do grupo de recursos para o qual esse cmdlet move recursos.</span><span class="sxs-lookup"><span data-stu-id="ec09b-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="ec09b-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec09b-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="ec09b-122">Especifica a ID da assinatura para a qual este cmdlet move recursos.</span><span class="sxs-lookup"><span data-stu-id="ec09b-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="ec09b-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="ec09b-123">-Force</span></span>
<span data-ttu-id="ec09b-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ec09b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec09b-125">-Pré-</span><span class="sxs-lookup"><span data-stu-id="ec09b-125">-Pre</span></span>
<span data-ttu-id="ec09b-126">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="ec09b-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ec09b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec09b-127">-ResourceId</span></span>
<span data-ttu-id="ec09b-128">Especifica uma matriz de IDs dos recursos que esse cmdlet move.</span><span class="sxs-lookup"><span data-stu-id="ec09b-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="ec09b-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ec09b-129">-Confirm</span></span>
<span data-ttu-id="ec09b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec09b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec09b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec09b-131">-WhatIf</span></span>
<span data-ttu-id="ec09b-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ec09b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec09b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec09b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec09b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec09b-134">CommonParameters</span></span>
<span data-ttu-id="ec09b-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec09b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec09b-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec09b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec09b-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="ec09b-137">INPUTS</span></span>

### <span data-ttu-id="ec09b-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec09b-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec09b-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ec09b-139">System.String[]</span></span>

## <span data-ttu-id="ec09b-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="ec09b-140">OUTPUTS</span></span>

### <span data-ttu-id="ec09b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec09b-141">System.Boolean</span></span>

## <span data-ttu-id="ec09b-142">Notas</span><span class="sxs-lookup"><span data-stu-id="ec09b-142">NOTES</span></span>

## <span data-ttu-id="ec09b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec09b-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec09b-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ec09b-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="ec09b-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="ec09b-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="ec09b-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="ec09b-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="ec09b-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="ec09b-147">Set-AzResource</span></span>](./Set-AzResource.md)


