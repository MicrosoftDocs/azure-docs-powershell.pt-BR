---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 5766c93ba1fa7434b6ebd41f0c414f5e8a9a5073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890510"
---
# <span data-ttu-id="8e9a7-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8e9a7-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8e9a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9a7-103">Atualiza as configurações avançadas de proteção contra ameaças em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="8e9a7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8e9a7-104">SYNTAX</span></span>

### <span data-ttu-id="8e9a7-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e9a7-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9a7-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9a7-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9a7-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9a7-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9a7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8e9a7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e9a7-109">O cmdlet **Update-AzSynapseSqlAdvancedThreatProtectionSetting** atualiza uma configuração avançada de proteção contra ameaças em um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="8e9a7-110">Para habilitar a proteção avançada contra ameaças em um espaço de trabalho, as configurações de auditoria devem ser habilitadas nesse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="8e9a7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e9a7-111">EXAMPLES</span></span>

### <span data-ttu-id="8e9a7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e9a7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="8e9a7-113">Este comando atualiza as configurações avançadas de proteção contra ameaças para um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8e9a7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8e9a7-114">PARAMETERS</span></span>

### <span data-ttu-id="8e9a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e9a7-115">-AsJob</span></span>
<span data-ttu-id="8e9a7-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8e9a7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e9a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9a7-117">-DefaultProfile</span></span>
<span data-ttu-id="8e9a7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e9a7-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="8e9a7-119">-EmailAdmin</span></span>
<span data-ttu-id="8e9a7-120">Define se os administradores de email serão definidos.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="8e9a7-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="8e9a7-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="8e9a7-122">Tipos de detecção a excluir.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="8e9a7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e9a7-123">-InputObject</span></span>
<span data-ttu-id="8e9a7-124">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a7-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="8e9a7-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="8e9a7-126">Uma lista separada por ponto-e-vírgula de endereços de email para o envio dos alertas.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="8e9a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e9a7-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-128">Resource group name.</span></span>

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

### <span data-ttu-id="8e9a7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9a7-129">-ResourceId</span></span>
<span data-ttu-id="8e9a7-130">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e9a7-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8e9a7-131">-RetentionInDays</span></span>
<span data-ttu-id="8e9a7-132">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="8e9a7-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e9a7-133">-StorageAccountName</span></span>
<span data-ttu-id="8e9a7-134">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="8e9a7-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e9a7-135">-WorkspaceName</span></span>
<span data-ttu-id="8e9a7-136">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e9a7-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e9a7-137">-Confirm</span></span>
<span data-ttu-id="8e9a7-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9a7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9a7-139">-WhatIf</span></span>
<span data-ttu-id="8e9a7-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9a7-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9a7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9a7-142">CommonParameters</span></span>
<span data-ttu-id="8e9a7-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9a7-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e9a7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9a7-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e9a7-145">INPUTS</span></span>

### <span data-ttu-id="8e9a7-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e9a7-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8e9a7-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8e9a7-147">OUTPUTS</span></span>

### <span data-ttu-id="8e9a7-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="8e9a7-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="8e9a7-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="8e9a7-149">NOTES</span></span>

## <span data-ttu-id="8e9a7-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e9a7-150">RELATED LINKS</span></span>
