---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 86bc4b8bedbaafb6da1267d94ffa01b3d0ca95c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428427"
---
# <span data-ttu-id="2d7a9-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="2d7a9-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="2d7a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7a9-103">Adiciona uma fonte de dados a computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d7a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d7a9-104">SYNTAX</span></span>

### <span data-ttu-id="2d7a9-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2d7a9-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7a9-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d7a9-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7a9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d7a9-107">DESCRIPTION</span></span>
<span data-ttu-id="2d7a9-108">O cmdlet **New-AzureRmOperationalInsightsLinuxSyslogDataSource** adiciona uma fonte de dados syslog a computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="2d7a9-109">O Azure Operational insights pode coletar dados de syslog.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="2d7a9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d7a9-110">EXAMPLES</span></span>

## <span data-ttu-id="2d7a9-111">OS</span><span class="sxs-lookup"><span data-stu-id="2d7a9-111">PARAMETERS</span></span>

### <span data-ttu-id="2d7a9-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="2d7a9-112">-CollectAlert</span></span>
<span data-ttu-id="2d7a9-113">Indica que as insights operacionais coletam mensagens de alerta.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="2d7a9-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="2d7a9-114">-CollectCritical</span></span>
<span data-ttu-id="2d7a9-115">Indica que as insights operacionais coletam mensagens críticas.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="2d7a9-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="2d7a9-116">-CollectDebug</span></span>
<span data-ttu-id="2d7a9-117">Indica que as insights operacionais coletam mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="2d7a9-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="2d7a9-118">-CollectEmergency</span></span>
<span data-ttu-id="2d7a9-119">Indica que as insights operacionais coletam mensagens de emergência.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="2d7a9-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="2d7a9-120">-CollectError</span></span>
<span data-ttu-id="2d7a9-121">Indica que as insights operacionais coletam mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="2d7a9-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="2d7a9-122">-CollectInformational</span></span>
<span data-ttu-id="2d7a9-123">Indica que as insights operacionais coletam mensagens informativas.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="2d7a9-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="2d7a9-124">-CollectNotice</span></span>
<span data-ttu-id="2d7a9-125">Indica que as insights operacionais coletam mensagens de aviso.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="2d7a9-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="2d7a9-126">-CollectWarning</span></span>
<span data-ttu-id="2d7a9-127">Indica que o syslog inclui mensagens de aviso.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="2d7a9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7a9-128">-DefaultProfile</span></span>
<span data-ttu-id="2d7a9-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2d7a9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d7a9-130">-Instalação</span><span class="sxs-lookup"><span data-stu-id="2d7a9-130">-Facility</span></span>
<span data-ttu-id="2d7a9-131">Especifica um código de instalação.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="2d7a9-132">-Force</span><span class="sxs-lookup"><span data-stu-id="2d7a9-132">-Force</span></span>
<span data-ttu-id="2d7a9-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d7a9-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d7a9-134">-Name</span></span>
<span data-ttu-id="2d7a9-135">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="2d7a9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7a9-136">-ResourceGroupName</span></span>
<span data-ttu-id="2d7a9-137">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="2d7a9-138">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="2d7a9-138">-Workspace</span></span>
<span data-ttu-id="2d7a9-139">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d7a9-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d7a9-140">-WorkspaceName</span></span>
<span data-ttu-id="2d7a9-141">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d7a9-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d7a9-142">-Confirm</span></span>
<span data-ttu-id="2d7a9-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7a9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7a9-144">-WhatIf</span></span>
<span data-ttu-id="2d7a9-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d7a9-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7a9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7a9-147">CommonParameters</span></span>
<span data-ttu-id="2d7a9-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7a9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7a9-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7a9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7a9-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d7a9-150">INPUTS</span></span>

### <span data-ttu-id="2d7a9-151">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d7a9-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="2d7a9-152">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d7a9-152">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="2d7a9-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2d7a9-153">System.String</span></span>

## <span data-ttu-id="2d7a9-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d7a9-154">OUTPUTS</span></span>

### <span data-ttu-id="2d7a9-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2d7a9-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2d7a9-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d7a9-156">NOTES</span></span>

## <span data-ttu-id="2d7a9-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d7a9-157">RELATED LINKS</span></span>

[<span data-ttu-id="2d7a9-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="2d7a9-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="2d7a9-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="2d7a9-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


