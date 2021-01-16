---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271268"
---
# <span data-ttu-id="726f3-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="726f3-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="726f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="726f3-102">SYNOPSIS</span></span>
<span data-ttu-id="726f3-103">Define as configurações avançadas de proteção contra ameaças em um pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="726f3-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="726f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="726f3-104">SYNTAX</span></span>

### <span data-ttu-id="726f3-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="726f3-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726f3-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="726f3-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726f3-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="726f3-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726f3-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="726f3-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="726f3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="726f3-109">DESCRIPTION</span></span>
<span data-ttu-id="726f3-110">O cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** define as configurações avançadas de proteção contra ameaças em um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="726f3-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="726f3-111">Para habilitar a proteção avançada contra ameaças em um pool SQL, as configurações de auditoria devem estar habilitadas nesse pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="726f3-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="726f3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="726f3-112">EXAMPLES</span></span>

### <span data-ttu-id="726f3-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="726f3-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="726f3-114">Esse comando define as configurações avançadas de proteção contra ameaças para um pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="726f3-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="726f3-115">OS</span><span class="sxs-lookup"><span data-stu-id="726f3-115">PARAMETERS</span></span>

### <span data-ttu-id="726f3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="726f3-116">-AsJob</span></span>
<span data-ttu-id="726f3-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="726f3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="726f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726f3-118">-DefaultProfile</span></span>
<span data-ttu-id="726f3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="726f3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="726f3-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="726f3-120">-EmailAdmin</span></span>
<span data-ttu-id="726f3-121">Define se os administradores de email devem ser enviados.</span><span class="sxs-lookup"><span data-stu-id="726f3-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="726f3-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="726f3-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="726f3-123">Tipos de detecção a serem excluídos.</span><span class="sxs-lookup"><span data-stu-id="726f3-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="726f3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="726f3-124">-InputObject</span></span>
<span data-ttu-id="726f3-125">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="726f3-125">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="726f3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="726f3-126">-Name</span></span>
<span data-ttu-id="726f3-127">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="726f3-127">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="726f3-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="726f3-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="726f3-129">Uma lista de endereços de email separados por ponto-e-vírgula para enviar os alertas.</span><span class="sxs-lookup"><span data-stu-id="726f3-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="726f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="726f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="726f3-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="726f3-131">Resource group name.</span></span>

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

### <span data-ttu-id="726f3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="726f3-132">-ResourceId</span></span>
<span data-ttu-id="726f3-133">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="726f3-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="726f3-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="726f3-134">-RetentionInDays</span></span>
<span data-ttu-id="726f3-135">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="726f3-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="726f3-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="726f3-136">-StorageAccountName</span></span>
<span data-ttu-id="726f3-137">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="726f3-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="726f3-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="726f3-138">-WorkspaceName</span></span>
<span data-ttu-id="726f3-139">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="726f3-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="726f3-140">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="726f3-140">-WorkspaceObject</span></span>
<span data-ttu-id="726f3-141">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="726f3-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="726f3-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="726f3-142">-Confirm</span></span>
<span data-ttu-id="726f3-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726f3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="726f3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="726f3-144">-WhatIf</span></span>
<span data-ttu-id="726f3-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="726f3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="726f3-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="726f3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="726f3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726f3-147">CommonParameters</span></span>
<span data-ttu-id="726f3-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="726f3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726f3-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="726f3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726f3-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="726f3-150">INPUTS</span></span>

### <span data-ttu-id="726f3-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="726f3-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="726f3-152">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="726f3-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="726f3-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="726f3-153">OUTPUTS</span></span>

### <span data-ttu-id="726f3-154">Microsoft. Azure. Commands. Synapse. Models. PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="726f3-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="726f3-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="726f3-155">NOTES</span></span>

## <span data-ttu-id="726f3-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="726f3-156">RELATED LINKS</span></span>
