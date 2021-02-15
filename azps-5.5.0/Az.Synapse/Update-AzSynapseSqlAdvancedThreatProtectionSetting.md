---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118870"
---
# <span data-ttu-id="adb90-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="adb90-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="adb90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adb90-102">SYNOPSIS</span></span>
<span data-ttu-id="adb90-103">Atualiza as configurações avançadas de proteção contra ameaças em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="adb90-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="adb90-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adb90-104">SYNTAX</span></span>

### <span data-ttu-id="adb90-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="adb90-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb90-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adb90-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adb90-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adb90-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adb90-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="adb90-108">DESCRIPTION</span></span>
<span data-ttu-id="adb90-109">O cmdlet **Update-AzSynapseSqlAdvancedThreatProtectionSetting** atualiza as configurações avançadas de proteção contra ameaças em um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="adb90-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="adb90-110">Para habilitar a proteção avançada contra ameaças em um espaço de trabalho, as configurações de auditoria devem ser habilitadas nesse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="adb90-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="adb90-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="adb90-111">EXAMPLES</span></span>

### <span data-ttu-id="adb90-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="adb90-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="adb90-113">Esse comando atualiza as configurações avançadas de proteção contra ameaças para um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="adb90-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="adb90-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adb90-114">PARAMETERS</span></span>

### <span data-ttu-id="adb90-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adb90-115">-AsJob</span></span>
<span data-ttu-id="adb90-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="adb90-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="adb90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb90-117">-DefaultProfile</span></span>
<span data-ttu-id="adb90-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adb90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb90-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="adb90-119">-EmailAdmin</span></span>
<span data-ttu-id="adb90-120">Define se os administradores de email podem fazer isso.</span><span class="sxs-lookup"><span data-stu-id="adb90-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="adb90-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="adb90-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="adb90-122">Tipos de detecção a ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="adb90-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="adb90-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adb90-123">-InputObject</span></span>
<span data-ttu-id="adb90-124">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="adb90-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="adb90-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="adb90-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="adb90-126">Uma lista de endereços de email separados por ponto e vírgula para enviar os alertas.</span><span class="sxs-lookup"><span data-stu-id="adb90-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="adb90-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb90-127">-ResourceGroupName</span></span>
<span data-ttu-id="adb90-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adb90-128">Resource group name.</span></span>

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

### <span data-ttu-id="adb90-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adb90-129">-ResourceId</span></span>
<span data-ttu-id="adb90-130">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="adb90-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="adb90-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="adb90-131">-RetentionInDays</span></span>
<span data-ttu-id="adb90-132">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="adb90-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="adb90-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="adb90-133">-StorageAccountName</span></span>
<span data-ttu-id="adb90-134">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="adb90-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="adb90-135">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="adb90-135">-WorkspaceName</span></span>
<span data-ttu-id="adb90-136">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="adb90-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="adb90-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="adb90-137">-Confirm</span></span>
<span data-ttu-id="adb90-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb90-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb90-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb90-139">-WhatIf</span></span>
<span data-ttu-id="adb90-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="adb90-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb90-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="adb90-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb90-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb90-142">CommonParameters</span></span>
<span data-ttu-id="adb90-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb90-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb90-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adb90-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb90-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="adb90-145">INPUTS</span></span>

### <span data-ttu-id="adb90-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="adb90-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="adb90-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="adb90-147">OUTPUTS</span></span>

### <span data-ttu-id="adb90-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="adb90-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="adb90-149">Notas</span><span class="sxs-lookup"><span data-stu-id="adb90-149">NOTES</span></span>

## <span data-ttu-id="adb90-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adb90-150">RELATED LINKS</span></span>
