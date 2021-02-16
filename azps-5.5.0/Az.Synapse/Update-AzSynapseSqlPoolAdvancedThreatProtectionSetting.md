---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118525"
---
# <span data-ttu-id="04ba8-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="04ba8-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="04ba8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="04ba8-103">Define configurações avançadas de proteção contra ameaças em um pool SQL.</span><span class="sxs-lookup"><span data-stu-id="04ba8-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="04ba8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04ba8-104">SYNTAX</span></span>

### <span data-ttu-id="04ba8-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="04ba8-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ba8-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ba8-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ba8-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ba8-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ba8-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ba8-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ba8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="04ba8-109">DESCRIPTION</span></span>
<span data-ttu-id="04ba8-110">O cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting define** uma configuração avançada de proteção contra ameaças em um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="04ba8-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="04ba8-111">Para habilitar a proteção avançada contra ameaças em um pool SQL, uma configuração de auditoria deve ser habilitada nesse pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="04ba8-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="04ba8-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04ba8-112">EXAMPLES</span></span>

### <span data-ttu-id="04ba8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04ba8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="04ba8-114">Esse comando define as configurações avançadas de proteção contra ameaças para um pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="04ba8-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="04ba8-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04ba8-115">PARAMETERS</span></span>

### <span data-ttu-id="04ba8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04ba8-116">-AsJob</span></span>
<span data-ttu-id="04ba8-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="04ba8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04ba8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ba8-118">-DefaultProfile</span></span>
<span data-ttu-id="04ba8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04ba8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ba8-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="04ba8-120">-EmailAdmin</span></span>
<span data-ttu-id="04ba8-121">Define se os administradores de email podem fazer isso.</span><span class="sxs-lookup"><span data-stu-id="04ba8-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="04ba8-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="04ba8-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="04ba8-123">Tipos de detecção a ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="04ba8-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="04ba8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04ba8-124">-InputObject</span></span>
<span data-ttu-id="04ba8-125">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="04ba8-125">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="04ba8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="04ba8-126">-Name</span></span>
<span data-ttu-id="04ba8-127">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="04ba8-127">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="04ba8-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="04ba8-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="04ba8-129">Uma lista de endereços de email separados por ponto e vírgula para enviar os alertas.</span><span class="sxs-lookup"><span data-stu-id="04ba8-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="04ba8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ba8-130">-ResourceGroupName</span></span>
<span data-ttu-id="04ba8-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04ba8-131">Resource group name.</span></span>

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

### <span data-ttu-id="04ba8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04ba8-132">-ResourceId</span></span>
<span data-ttu-id="04ba8-133">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="04ba8-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="04ba8-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="04ba8-134">-RetentionInDays</span></span>
<span data-ttu-id="04ba8-135">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="04ba8-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="04ba8-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04ba8-136">-StorageAccountName</span></span>
<span data-ttu-id="04ba8-137">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="04ba8-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="04ba8-138">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="04ba8-138">-WorkspaceName</span></span>
<span data-ttu-id="04ba8-139">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="04ba8-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="04ba8-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="04ba8-140">-WorkspaceObject</span></span>
<span data-ttu-id="04ba8-141">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="04ba8-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="04ba8-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="04ba8-142">-Confirm</span></span>
<span data-ttu-id="04ba8-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04ba8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ba8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ba8-144">-WhatIf</span></span>
<span data-ttu-id="04ba8-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="04ba8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ba8-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04ba8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ba8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ba8-147">CommonParameters</span></span>
<span data-ttu-id="04ba8-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ba8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ba8-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04ba8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ba8-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="04ba8-150">INPUTS</span></span>

### <span data-ttu-id="04ba8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="04ba8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="04ba8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="04ba8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="04ba8-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="04ba8-153">OUTPUTS</span></span>

### <span data-ttu-id="04ba8-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="04ba8-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="04ba8-155">Notas</span><span class="sxs-lookup"><span data-stu-id="04ba8-155">NOTES</span></span>

## <span data-ttu-id="04ba8-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04ba8-156">RELATED LINKS</span></span>
