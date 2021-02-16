---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113402"
---
# <span data-ttu-id="1cf91-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="1cf91-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="1cf91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cf91-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf91-103">Adiciona uma fonte de dados a computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="1cf91-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="1cf91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cf91-104">SYNTAX</span></span>

### <span data-ttu-id="1cf91-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1cf91-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf91-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1cf91-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cf91-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cf91-107">DESCRIPTION</span></span>
<span data-ttu-id="1cf91-108">O cmdlet **New-AzOperationalInsightsLinuxSyslogDataSource** adiciona uma fonte de dados syslog a computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cf91-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="1cf91-109">O Insights Operacionais do Azure pode coletar dados de syslog.</span><span class="sxs-lookup"><span data-stu-id="1cf91-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="1cf91-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1cf91-110">EXAMPLES</span></span>

### <span data-ttu-id="1cf91-111">Exemplo 1: Criar fontes de dados de syslog</span><span class="sxs-lookup"><span data-stu-id="1cf91-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="1cf91-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cf91-112">PARAMETERS</span></span>

### <span data-ttu-id="1cf91-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="1cf91-113">-CollectAlert</span></span>
<span data-ttu-id="1cf91-114">Indica que o Insights Operacionais coleta mensagens de alerta.</span><span class="sxs-lookup"><span data-stu-id="1cf91-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="1cf91-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="1cf91-115">-CollectCritical</span></span>
<span data-ttu-id="1cf91-116">Indica que o Insights Operacionais coleta mensagens críticas.</span><span class="sxs-lookup"><span data-stu-id="1cf91-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="1cf91-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="1cf91-117">-CollectDebug</span></span>
<span data-ttu-id="1cf91-118">Indica que o Insights Operacionais coleta mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="1cf91-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="1cf91-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="1cf91-119">-CollectEmergency</span></span>
<span data-ttu-id="1cf91-120">Indica que o Insights Operacionais coleta mensagens de emergência.</span><span class="sxs-lookup"><span data-stu-id="1cf91-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="1cf91-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="1cf91-121">-CollectError</span></span>
<span data-ttu-id="1cf91-122">Indica que o Insights Operacionais coleta mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="1cf91-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="1cf91-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="1cf91-123">-CollectInformational</span></span>
<span data-ttu-id="1cf91-124">Indica que o Insights Operacionais coleta mensagens informativas.</span><span class="sxs-lookup"><span data-stu-id="1cf91-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="1cf91-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="1cf91-125">-CollectNotice</span></span>
<span data-ttu-id="1cf91-126">Indica que o Insights Operacionais coleta mensagens de aviso.</span><span class="sxs-lookup"><span data-stu-id="1cf91-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="1cf91-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="1cf91-127">-CollectWarning</span></span>
<span data-ttu-id="1cf91-128">Indica que o syslog inclui mensagens de aviso.</span><span class="sxs-lookup"><span data-stu-id="1cf91-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="1cf91-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf91-129">-DefaultProfile</span></span>
<span data-ttu-id="1cf91-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1cf91-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cf91-131">-Facilidade</span><span class="sxs-lookup"><span data-stu-id="1cf91-131">-Facility</span></span>
<span data-ttu-id="1cf91-132">Especifica um código de instalação.</span><span class="sxs-lookup"><span data-stu-id="1cf91-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="1cf91-133">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1cf91-133">-Force</span></span>
<span data-ttu-id="1cf91-134">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1cf91-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1cf91-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cf91-135">-Name</span></span>
<span data-ttu-id="1cf91-136">Especifica um nome para a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="1cf91-136">Specifies a name for the data source.</span></span> <span data-ttu-id="1cf91-137">O nome não é exposto no Portal do Azure e qualquer cadeia de caracteres pode ser usada desde que seja exclusiva.</span><span class="sxs-lookup"><span data-stu-id="1cf91-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="1cf91-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf91-138">-ResourceGroupName</span></span>
<span data-ttu-id="1cf91-139">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="1cf91-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="1cf91-140">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1cf91-140">-Workspace</span></span>
<span data-ttu-id="1cf91-141">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="1cf91-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1cf91-142">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1cf91-142">-WorkspaceName</span></span>
<span data-ttu-id="1cf91-143">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="1cf91-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1cf91-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1cf91-144">-Confirm</span></span>
<span data-ttu-id="1cf91-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cf91-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cf91-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cf91-146">-WhatIf</span></span>
<span data-ttu-id="1cf91-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1cf91-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cf91-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cf91-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cf91-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf91-149">CommonParameters</span></span>
<span data-ttu-id="1cf91-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cf91-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf91-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf91-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf91-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="1cf91-152">INPUTS</span></span>

### <span data-ttu-id="1cf91-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1cf91-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="1cf91-154">System.String</span><span class="sxs-lookup"><span data-stu-id="1cf91-154">System.String</span></span>

## <span data-ttu-id="1cf91-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="1cf91-155">OUTPUTS</span></span>

### <span data-ttu-id="1cf91-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1cf91-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1cf91-157">Notas</span><span class="sxs-lookup"><span data-stu-id="1cf91-157">NOTES</span></span>

## <span data-ttu-id="1cf91-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cf91-158">RELATED LINKS</span></span>

[<span data-ttu-id="1cf91-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="1cf91-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="1cf91-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="1cf91-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


