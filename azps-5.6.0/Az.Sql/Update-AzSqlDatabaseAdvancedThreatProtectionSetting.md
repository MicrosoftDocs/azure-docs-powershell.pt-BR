---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9677f45e772cbcb48190f5792df97e96051180c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890561"
---
# <span data-ttu-id="4b270-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="4b270-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="4b270-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b270-102">SYNOPSIS</span></span>
<span data-ttu-id="4b270-103">Define configurações avançadas de proteção contra ameaças em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b270-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="4b270-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4b270-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b270-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4b270-105">DESCRIPTION</span></span>
<span data-ttu-id="4b270-106">O cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** define uma configuração avançada de proteção contra ameaças em um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4b270-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="4b270-107">Para habilitar a proteção avançada contra ameaças em um banco de dados, as configurações de auditoria devem ser habilitadas nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b270-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="4b270-108">Para usar esse cmdlet, especifique os *parâmetros ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b270-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="4b270-109">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="4b270-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4b270-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b270-110">EXAMPLES</span></span>

### <span data-ttu-id="4b270-111">Exemplo 1: definir as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="4b270-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="4b270-112">Este comando define as configurações avançadas de proteção contra ameaças para um banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="4b270-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="4b270-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4b270-113">PARAMETERS</span></span>

### <span data-ttu-id="4b270-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b270-114">-DatabaseName</span></span>
<span data-ttu-id="4b270-115">Especifica o nome do banco de dados onde as configurações estão definidas.</span><span class="sxs-lookup"><span data-stu-id="4b270-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="4b270-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b270-116">-DefaultProfile</span></span>
<span data-ttu-id="4b270-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4b270-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b270-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="4b270-118">-EmailAdmins</span></span>
<span data-ttu-id="4b270-119">Especifica se as configurações avançadas de proteção contra ameaças contatarão administradores usando email.</span><span class="sxs-lookup"><span data-stu-id="4b270-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="4b270-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="4b270-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="4b270-121">Especifica uma matriz de tipos de detecção a ser excluída das configurações.</span><span class="sxs-lookup"><span data-stu-id="4b270-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="4b270-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4b270-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4b270-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="4b270-123">Sql_Injection</span></span> 
- <span data-ttu-id="4b270-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="4b270-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="4b270-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="4b270-125">Access_Anomaly</span></span> 
- <span data-ttu-id="4b270-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4b270-126">None</span></span>

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

### <span data-ttu-id="4b270-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="4b270-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="4b270-128">Especifica uma lista separada por ponto-e-vírgula de endereços de email para os quais as configurações enviam alertas.</span><span class="sxs-lookup"><span data-stu-id="4b270-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="4b270-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b270-129">-PassThru</span></span>
<span data-ttu-id="4b270-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4b270-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4b270-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4b270-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4b270-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b270-132">-ResourceGroupName</span></span>
<span data-ttu-id="4b270-133">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="4b270-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4b270-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4b270-134">-RetentionInDays</span></span>
<span data-ttu-id="4b270-135">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="4b270-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="4b270-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4b270-136">-ServerName</span></span>
<span data-ttu-id="4b270-137">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b270-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4b270-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4b270-138">-StorageAccountName</span></span>
<span data-ttu-id="4b270-139">Especifica o nome da conta de armazenamento a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4b270-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="4b270-140">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="4b270-140">Wildcards are not permitted.</span></span> <span data-ttu-id="4b270-141">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="4b270-141">This parameter is not required.</span></span> <span data-ttu-id="4b270-142">Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte das configurações avançadas de proteção contra ameaças do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b270-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="4b270-143">Se essa for a primeira vez que as configurações avançadas de proteção contra ameaças do banco de dados são definidas e esse parâmetro não é fornecido, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="4b270-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="4b270-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b270-144">-Confirm</span></span>
<span data-ttu-id="4b270-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b270-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b270-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b270-146">-WhatIf</span></span>
<span data-ttu-id="4b270-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b270-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b270-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b270-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b270-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b270-149">CommonParameters</span></span>
<span data-ttu-id="4b270-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b270-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b270-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b270-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b270-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b270-152">INPUTS</span></span>

### <span data-ttu-id="4b270-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4b270-153">System.String</span></span>

### <span data-ttu-id="4b270-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b270-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4b270-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="4b270-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="4b270-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b270-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4b270-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4b270-157">OUTPUTS</span></span>

### <span data-ttu-id="4b270-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="4b270-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="4b270-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="4b270-159">NOTES</span></span>

## <span data-ttu-id="4b270-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b270-160">RELATED LINKS</span></span>

[<span data-ttu-id="4b270-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="4b270-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="4b270-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="4b270-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="4b270-163">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="4b270-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


