---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 079a1254865821b77ca48a94256dbe1a9e4cb431
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415318"
---
# <span data-ttu-id="e95d3-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e95d3-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e95d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e95d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e95d3-103">Define configurações avançadas de proteção contra ameaças em um servidor.</span><span class="sxs-lookup"><span data-stu-id="e95d3-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="e95d3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e95d3-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95d3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e95d3-105">DESCRIPTION</span></span>
<span data-ttu-id="e95d3-106">O cmdlet **Update-AzSqlServerAdvancedThreatProtectionSetting define** configurações avançadas de proteção contra ameaças em um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e95d3-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="e95d3-107">Para habilitar a proteção avançada contra ameaças em um servidor, as configurações de auditoria devem ser habilitadas nesse servidor.</span><span class="sxs-lookup"><span data-stu-id="e95d3-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="e95d3-108">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e ServerName para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="e95d3-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="e95d3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e95d3-109">EXAMPLES</span></span>

### <span data-ttu-id="e95d3-110">Exemplo 1: Definir as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="e95d3-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e95d3-111">Esse comando define as configurações avançadas de proteção contra ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="e95d3-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="e95d3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e95d3-112">PARAMETERS</span></span>

### <span data-ttu-id="e95d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95d3-113">-DefaultProfile</span></span>
<span data-ttu-id="e95d3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e95d3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e95d3-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e95d3-115">-EmailAdmins</span></span>
<span data-ttu-id="e95d3-116">Especifica se as configurações avançadas de proteção contra ameaças contatam os administradores usando o email.</span><span class="sxs-lookup"><span data-stu-id="e95d3-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e95d3-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="e95d3-118">Especifica uma matriz de tipos de detecção a ser excluída das configurações.</span><span class="sxs-lookup"><span data-stu-id="e95d3-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="e95d3-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e95d3-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e95d3-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e95d3-120">Sql_Injection</span></span>
- <span data-ttu-id="e95d3-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e95d3-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="e95d3-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e95d3-122">Access_Anomaly</span></span>
- <span data-ttu-id="e95d3-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e95d3-123">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e95d3-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e95d3-125">Especifica uma lista separada por ponto e vírgula de endereços de email para os quais as configurações enviam alertas.</span><span class="sxs-lookup"><span data-stu-id="e95d3-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="e95d3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e95d3-126">-PassThru</span></span>
<span data-ttu-id="e95d3-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e95d3-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e95d3-128">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="e95d3-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e95d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="e95d3-130">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="e95d3-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="e95d3-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e95d3-131">-RetentionInDays</span></span>
<span data-ttu-id="e95d3-132">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="e95d3-132">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e95d3-133">-ServerName</span></span>
<span data-ttu-id="e95d3-134">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e95d3-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d3-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e95d3-135">-StorageAccountName</span></span>
<span data-ttu-id="e95d3-136">Especifica o nome da conta de armazenamento a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e95d3-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e95d3-137">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="e95d3-137">Wildcards are not permitted.</span></span> <span data-ttu-id="e95d3-138">Este parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="e95d3-138">This parameter is not required.</span></span> <span data-ttu-id="e95d3-139">Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte das configurações avançadas de proteção contra ameaças do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e95d3-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="e95d3-140">Se esta for a primeira vez que as configurações de detecção de ameaças de banco de dados são definidas e esse parâmetro não é fornecido, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="e95d3-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e95d3-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e95d3-141">-Confirm</span></span>
<span data-ttu-id="e95d3-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95d3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95d3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95d3-143">-WhatIf</span></span>
<span data-ttu-id="e95d3-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e95d3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95d3-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e95d3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95d3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95d3-146">CommonParameters</span></span>
<span data-ttu-id="e95d3-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95d3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95d3-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e95d3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95d3-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="e95d3-149">INPUTS</span></span>

### <span data-ttu-id="e95d3-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e95d3-150">System.String</span></span>

### <span data-ttu-id="e95d3-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e95d3-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e95d3-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="e95d3-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="e95d3-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e95d3-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e95d3-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="e95d3-154">OUTPUTS</span></span>

### <span data-ttu-id="e95d3-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="e95d3-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="e95d3-156">Notas</span><span class="sxs-lookup"><span data-stu-id="e95d3-156">NOTES</span></span>

## <span data-ttu-id="e95d3-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e95d3-157">RELATED LINKS</span></span>

[<span data-ttu-id="e95d3-158">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e95d3-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
