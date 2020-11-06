---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 83f9ec56f5d33b65810da96364ab11dd4eb7c52a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429179"
---
# <span data-ttu-id="26626-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="26626-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="26626-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26626-102">SYNOPSIS</span></span>
<span data-ttu-id="26626-103">Cria um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="26626-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26626-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26626-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26626-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26626-105">DESCRIPTION</span></span>
<span data-ttu-id="26626-106">O cmdlet **New-AzureRmOperationalInsightsWorkspace** cria um espaço de trabalho no grupo de recursos e na localização especificados.</span><span class="sxs-lookup"><span data-stu-id="26626-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="26626-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26626-107">EXAMPLES</span></span>

### <span data-ttu-id="26626-108">Exemplo 1: criar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="26626-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="26626-109">Esse comando cria um espaço de trabalho de SKU padrão chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="26626-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="26626-110">Exemplo 2: criar um espaço de trabalho e vinculá-lo a uma conta existente</span><span class="sxs-lookup"><span data-stu-id="26626-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="26626-111">O primeiro comando usa o cmdlet Get-AzureRmOperationalInsightsLinkTargets para obter destinos de link de conta de insights operacionais e, em seguida, armazena-os na variável $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="26626-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="26626-112">O segundo comando passa o destino do link da primeira conta no $OILinkTargets para o cmdlet **New-AzureRmOperationalInsightsWorkspace** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="26626-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="26626-113">O comando cria um espaço de trabalho de SKU padrão chamado MyWorkspace que está vinculado à primeira conta de insights operacionais em $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="26626-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="26626-114">OS</span><span class="sxs-lookup"><span data-stu-id="26626-114">PARAMETERS</span></span>

### <span data-ttu-id="26626-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="26626-115">-CustomerId</span></span>
<span data-ttu-id="26626-116">Especifica a conta para a qual esse espaço de trabalho será vinculado.</span><span class="sxs-lookup"><span data-stu-id="26626-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="26626-117">O cmdlet Get-AzureRmOperationalInsightsLinkTargets também pode ser usado para listar as contas potenciais.</span><span class="sxs-lookup"><span data-stu-id="26626-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26626-118">-Force</span><span class="sxs-lookup"><span data-stu-id="26626-118">-Force</span></span>
<span data-ttu-id="26626-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="26626-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26626-120">-Local</span><span class="sxs-lookup"><span data-stu-id="26626-120">-Location</span></span>
<span data-ttu-id="26626-121">Especifica o local no qual criar o espaço de trabalho, por exemplo, leste EUA ou oeste europeu.</span><span class="sxs-lookup"><span data-stu-id="26626-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26626-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="26626-122">-Name</span></span>
<span data-ttu-id="26626-123">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="26626-123">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26626-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26626-124">-ResourceGroupName</span></span>
<span data-ttu-id="26626-125">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="26626-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="26626-126">O espaço de trabalho é criado neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26626-126">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26626-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="26626-127">-Sku</span></span>
<span data-ttu-id="26626-128">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="26626-128">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="26626-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="26626-129">Valid values are:</span></span> 

- <span data-ttu-id="26626-130">gratuito</span><span class="sxs-lookup"><span data-stu-id="26626-130">free</span></span>
- <span data-ttu-id="26626-131">oficial</span><span class="sxs-lookup"><span data-stu-id="26626-131">standard</span></span>
- <span data-ttu-id="26626-132">gratifica</span><span class="sxs-lookup"><span data-stu-id="26626-132">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26626-133">-Marcas</span><span class="sxs-lookup"><span data-stu-id="26626-133">-Tags</span></span>
<span data-ttu-id="26626-134">Especifica as marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="26626-134">Specifies the resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26626-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26626-135">-Confirm</span></span>
<span data-ttu-id="26626-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26626-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26626-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26626-137">-WhatIf</span></span>
<span data-ttu-id="26626-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26626-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26626-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26626-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26626-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26626-140">-DefaultProfile</span></span>
<span data-ttu-id="26626-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26626-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26626-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="26626-142">-RetentionInDays</span></span>
<span data-ttu-id="26626-143">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="26626-143">The workspace data retention in days.</span></span> <span data-ttu-id="26626-144">730 dias é o máximo permitido para todas as outras SKUs.</span><span class="sxs-lookup"><span data-stu-id="26626-144">730 days is the maximum allowed for all other Skus.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26626-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26626-145">CommonParameters</span></span>
<span data-ttu-id="26626-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26626-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26626-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26626-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26626-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26626-148">INPUTS</span></span>

## <span data-ttu-id="26626-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26626-149">OUTPUTS</span></span>

### <span data-ttu-id="26626-150">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="26626-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="26626-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26626-151">NOTES</span></span>

## <span data-ttu-id="26626-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26626-152">RELATED LINKS</span></span>

[<span data-ttu-id="26626-153">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="26626-153">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="26626-154">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="26626-154">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


