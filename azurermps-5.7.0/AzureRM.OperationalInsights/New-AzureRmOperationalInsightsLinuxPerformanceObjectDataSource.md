---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: decae9e9282ad85832df676162f6bc684684f339
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610913"
---
# <span data-ttu-id="ca35d-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="ca35d-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="ca35d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca35d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca35d-103">Adiciona contadores de desempenho a todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca35d-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca35d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca35d-104">SYNTAX</span></span>

### <span data-ttu-id="ca35d-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca35d-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca35d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ca35d-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca35d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca35d-107">DESCRIPTION</span></span>
<span data-ttu-id="ca35d-108">O cmdlet **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** adiciona contadores de desempenho dos quais o Azure Operational insights coleta dados para todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca35d-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="ca35d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca35d-109">EXAMPLES</span></span>

## <span data-ttu-id="ca35d-110">OS</span><span class="sxs-lookup"><span data-stu-id="ca35d-110">PARAMETERS</span></span>

### <span data-ttu-id="ca35d-111">-Nomes prenomeados</span><span class="sxs-lookup"><span data-stu-id="ca35d-111">-CounterNames</span></span>
<span data-ttu-id="ca35d-112">Especifica uma matriz de nomes de contadores.</span><span class="sxs-lookup"><span data-stu-id="ca35d-112">Specifies an array of names of counters.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca35d-113">-DefaultProfile</span></span>
<span data-ttu-id="ca35d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ca35d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca35d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca35d-115">-Force</span></span>
<span data-ttu-id="ca35d-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ca35d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca35d-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ca35d-117">-InstanceName</span></span>
<span data-ttu-id="ca35d-118">Especifica um nome de instância.</span><span class="sxs-lookup"><span data-stu-id="ca35d-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ca35d-119">-IntervalSeconds</span></span>
<span data-ttu-id="ca35d-120">Especifica o intervalo da coleção.</span><span class="sxs-lookup"><span data-stu-id="ca35d-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca35d-121">-Name</span></span>
<span data-ttu-id="ca35d-122">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="ca35d-122">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="ca35d-123">-ObjectName</span></span>
<span data-ttu-id="ca35d-124">Especifica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ca35d-124">Specifies the name of an object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca35d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca35d-126">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="ca35d-126">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-127">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="ca35d-127">-Workspace</span></span>
<span data-ttu-id="ca35d-128">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="ca35d-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ca35d-129">-WorkspaceName</span></span>
<span data-ttu-id="ca35d-130">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="ca35d-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca35d-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca35d-131">-Confirm</span></span>
<span data-ttu-id="ca35d-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca35d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca35d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca35d-133">-WhatIf</span></span>
<span data-ttu-id="ca35d-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca35d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca35d-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca35d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca35d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca35d-136">CommonParameters</span></span>
<span data-ttu-id="ca35d-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca35d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca35d-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca35d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca35d-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca35d-139">INPUTS</span></span>

### <span data-ttu-id="ca35d-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ca35d-140">PSWorkspace</span></span>
<span data-ttu-id="ca35d-141">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ca35d-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="ca35d-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca35d-142">OUTPUTS</span></span>

### <span data-ttu-id="ca35d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ca35d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ca35d-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca35d-144">NOTES</span></span>

## <span data-ttu-id="ca35d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca35d-145">RELATED LINKS</span></span>

[<span data-ttu-id="ca35d-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="ca35d-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="ca35d-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="ca35d-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


