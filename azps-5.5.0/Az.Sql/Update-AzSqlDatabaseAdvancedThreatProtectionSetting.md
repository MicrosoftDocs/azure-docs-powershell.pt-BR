---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: baa3e3d4b272bccab5fe33b9af05edc9ed254236
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398896"
---
# <span data-ttu-id="7f392-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="7f392-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="7f392-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f392-102">SYNOPSIS</span></span>
<span data-ttu-id="7f392-103">Define configurações avançadas de proteção contra ameaças em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7f392-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="7f392-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f392-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f392-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f392-105">DESCRIPTION</span></span>
<span data-ttu-id="7f392-106">O cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting define** configurações avançadas de proteção contra ameaças em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f392-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="7f392-107">Para habilitar a proteção avançada contra ameaças em um banco de dados, é necessário habilitar as configurações de auditoria nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7f392-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="7f392-108">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7f392-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="7f392-109">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="7f392-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7f392-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f392-110">EXAMPLES</span></span>

### <span data-ttu-id="7f392-111">Exemplo 1: Definir as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="7f392-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="7f392-112">Esse comando define as configurações avançadas de proteção contra ameaças para um banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="7f392-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="7f392-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f392-113">PARAMETERS</span></span>

### <span data-ttu-id="7f392-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="7f392-114">-DatabaseName</span></span>
<span data-ttu-id="7f392-115">Especifica o nome do banco de dados onde as configurações estão definidas.</span><span class="sxs-lookup"><span data-stu-id="7f392-115">Specifies the name of the database where the settings is set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f392-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f392-116">-DefaultProfile</span></span>
<span data-ttu-id="7f392-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7f392-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f392-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7f392-118">-EmailAdmins</span></span>
<span data-ttu-id="7f392-119">Especifica se as configurações avançadas de proteção contra ameaças contatam os administradores usando o email.</span><span class="sxs-lookup"><span data-stu-id="7f392-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="7f392-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="7f392-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="7f392-121">Especifica uma matriz de tipos de detecção a ser excluída das configurações.</span><span class="sxs-lookup"><span data-stu-id="7f392-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="7f392-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f392-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f392-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="7f392-123">Sql_Injection</span></span>
- <span data-ttu-id="7f392-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="7f392-124">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="7f392-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="7f392-125">Access_Anomaly</span></span>
- <span data-ttu-id="7f392-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7f392-126">None</span></span>

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

### <span data-ttu-id="7f392-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="7f392-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="7f392-128">Especifica uma lista separada por ponto e vírgula dos endereços de email para os quais as configurações enviam alertas.</span><span class="sxs-lookup"><span data-stu-id="7f392-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="7f392-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f392-129">-PassThru</span></span>
<span data-ttu-id="7f392-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="7f392-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f392-131">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="7f392-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f392-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f392-132">-ResourceGroupName</span></span>
<span data-ttu-id="7f392-133">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="7f392-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7f392-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7f392-134">-RetentionInDays</span></span>
<span data-ttu-id="7f392-135">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="7f392-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="7f392-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f392-136">-ServerName</span></span>
<span data-ttu-id="7f392-137">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="7f392-137">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f392-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7f392-138">-StorageAccountName</span></span>
<span data-ttu-id="7f392-139">Especifica o nome da conta de armazenamento a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7f392-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="7f392-140">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="7f392-140">Wildcards are not permitted.</span></span> <span data-ttu-id="7f392-141">Este parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="7f392-141">This parameter is not required.</span></span> <span data-ttu-id="7f392-142">Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte das configurações avançadas de proteção contra ameaças do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7f392-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="7f392-143">Se esta for a primeira vez que as configurações avançadas de proteção contra ameaças do banco de dados são definidas e esse parâmetro não é fornecido, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="7f392-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="7f392-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7f392-144">-Confirm</span></span>
<span data-ttu-id="7f392-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f392-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f392-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f392-146">-WhatIf</span></span>
<span data-ttu-id="7f392-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7f392-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f392-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f392-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f392-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f392-149">CommonParameters</span></span>
<span data-ttu-id="7f392-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f392-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f392-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f392-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f392-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="7f392-152">INPUTS</span></span>

### <span data-ttu-id="7f392-153">System.String</span><span class="sxs-lookup"><span data-stu-id="7f392-153">System.String</span></span>

### <span data-ttu-id="7f392-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f392-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7f392-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="7f392-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="7f392-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f392-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7f392-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="7f392-157">OUTPUTS</span></span>

### <span data-ttu-id="7f392-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="7f392-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="7f392-159">Notas</span><span class="sxs-lookup"><span data-stu-id="7f392-159">NOTES</span></span>

## <span data-ttu-id="7f392-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f392-160">RELATED LINKS</span></span>

[<span data-ttu-id="7f392-161">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7f392-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
