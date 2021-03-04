---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 2267f9420e545fd693b734aaf8f90e89cce000a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890912"
---
# <span data-ttu-id="31290-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="31290-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="31290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31290-102">SYNOPSIS</span></span>
<span data-ttu-id="31290-103">Define configurações avançadas de proteção contra ameaças em um SQL pool.</span><span class="sxs-lookup"><span data-stu-id="31290-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="31290-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="31290-104">SYNTAX</span></span>

### <span data-ttu-id="31290-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="31290-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31290-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31290-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31290-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31290-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31290-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31290-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31290-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="31290-109">DESCRIPTION</span></span>
<span data-ttu-id="31290-110">O cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** define uma configuração avançada de proteção contra ameaças em um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="31290-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="31290-111">Para habilitar a proteção avançada contra ameaças em um pool SQL uma configuração de auditoria deve ser habilitada nesse pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="31290-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="31290-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31290-112">EXAMPLES</span></span>

### <span data-ttu-id="31290-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31290-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="31290-114">Este comando define as configurações avançadas de proteção contra ameaças para um pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="31290-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="31290-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="31290-115">PARAMETERS</span></span>

### <span data-ttu-id="31290-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31290-116">-AsJob</span></span>
<span data-ttu-id="31290-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="31290-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31290-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31290-118">-DefaultProfile</span></span>
<span data-ttu-id="31290-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31290-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31290-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="31290-120">-EmailAdmin</span></span>
<span data-ttu-id="31290-121">Define se os administradores de email serão definidos.</span><span class="sxs-lookup"><span data-stu-id="31290-121">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="31290-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="31290-123">Tipos de detecção a excluir.</span><span class="sxs-lookup"><span data-stu-id="31290-123">Detection types to exclude.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31290-124">-InputObject</span></span>
<span data-ttu-id="31290-125">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="31290-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31290-126">-Name</span><span class="sxs-lookup"><span data-stu-id="31290-126">-Name</span></span>
<span data-ttu-id="31290-127">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="31290-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="31290-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="31290-129">Uma lista separada por ponto-e-vírgula de endereços de email para o envio dos alertas.</span><span class="sxs-lookup"><span data-stu-id="31290-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31290-130">-ResourceGroupName</span></span>
<span data-ttu-id="31290-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31290-131">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31290-132">-ResourceId</span></span>
<span data-ttu-id="31290-133">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="31290-133">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="31290-134">-RetentionInDays</span></span>
<span data-ttu-id="31290-135">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="31290-135">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="31290-136">-StorageAccountName</span></span>
<span data-ttu-id="31290-137">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="31290-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="31290-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31290-138">-WorkspaceName</span></span>
<span data-ttu-id="31290-139">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="31290-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="31290-140">-WorkspaceObject</span></span>
<span data-ttu-id="31290-141">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="31290-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31290-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31290-142">-Confirm</span></span>
<span data-ttu-id="31290-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31290-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31290-144">-WhatIf</span></span>
<span data-ttu-id="31290-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31290-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31290-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31290-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31290-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31290-147">CommonParameters</span></span>
<span data-ttu-id="31290-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31290-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31290-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31290-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31290-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31290-150">INPUTS</span></span>

### <span data-ttu-id="31290-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="31290-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="31290-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="31290-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="31290-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="31290-153">OUTPUTS</span></span>

### <span data-ttu-id="31290-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="31290-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="31290-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="31290-155">NOTES</span></span>

## <span data-ttu-id="31290-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31290-156">RELATED LINKS</span></span>
