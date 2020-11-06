---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429187"
---
# <span data-ttu-id="041e2-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="041e2-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="041e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="041e2-102">SYNOPSIS</span></span>
<span data-ttu-id="041e2-103">Adiciona contadores de desempenho a todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="041e2-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="041e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="041e2-104">SYNTAX</span></span>

### <span data-ttu-id="041e2-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="041e2-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="041e2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="041e2-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="041e2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="041e2-107">DESCRIPTION</span></span>
<span data-ttu-id="041e2-108">O cmdlet **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** adiciona contadores de desempenho dos quais o Azure Operational insights coleta dados para todos os computadores Linux em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="041e2-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="041e2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="041e2-109">EXAMPLES</span></span>

## <span data-ttu-id="041e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="041e2-110">PARAMETERS</span></span>

### <span data-ttu-id="041e2-111">-Nomes prenomeados</span><span class="sxs-lookup"><span data-stu-id="041e2-111">-CounterNames</span></span>
<span data-ttu-id="041e2-112">Especifica uma matriz de nomes de contadores.</span><span class="sxs-lookup"><span data-stu-id="041e2-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041e2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="041e2-113">-Force</span></span>
<span data-ttu-id="041e2-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="041e2-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="041e2-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="041e2-115">-InstanceName</span></span>
<span data-ttu-id="041e2-116">Especifica um nome de instância.</span><span class="sxs-lookup"><span data-stu-id="041e2-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="041e2-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="041e2-117">-IntervalSeconds</span></span>
<span data-ttu-id="041e2-118">Especifica o intervalo da coleção.</span><span class="sxs-lookup"><span data-stu-id="041e2-118">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041e2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="041e2-119">-Name</span></span>
<span data-ttu-id="041e2-120">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="041e2-120">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041e2-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="041e2-121">-ObjectName</span></span>
<span data-ttu-id="041e2-122">Especifica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="041e2-122">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="041e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="041e2-124">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="041e2-124">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041e2-125">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="041e2-125">-Workspace</span></span>
<span data-ttu-id="041e2-126">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="041e2-126">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="041e2-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="041e2-127">-WorkspaceName</span></span>
<span data-ttu-id="041e2-128">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="041e2-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="041e2-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="041e2-129">-Confirm</span></span>
<span data-ttu-id="041e2-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="041e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="041e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="041e2-131">-WhatIf</span></span>
<span data-ttu-id="041e2-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="041e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="041e2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="041e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="041e2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="041e2-134">-DefaultProfile</span></span>
<span data-ttu-id="041e2-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="041e2-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="041e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="041e2-136">CommonParameters</span></span>
<span data-ttu-id="041e2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="041e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="041e2-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="041e2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="041e2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="041e2-139">INPUTS</span></span>

### <span data-ttu-id="041e2-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="041e2-140">PSWorkspace</span></span>
<span data-ttu-id="041e2-141">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="041e2-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="041e2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="041e2-142">OUTPUTS</span></span>

### <span data-ttu-id="041e2-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="041e2-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="041e2-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="041e2-144">NOTES</span></span>

## <span data-ttu-id="041e2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="041e2-145">RELATED LINKS</span></span>

[<span data-ttu-id="041e2-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="041e2-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="041e2-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="041e2-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


