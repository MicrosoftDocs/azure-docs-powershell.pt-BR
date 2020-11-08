---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111288"
---
# <span data-ttu-id="339a9-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="339a9-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="339a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="339a9-102">SYNOPSIS</span></span>
<span data-ttu-id="339a9-103">Define as configurações avançadas de proteção contra ameaças em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="339a9-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="339a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="339a9-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="339a9-105">DESCRIPTION</span></span>
<span data-ttu-id="339a9-106">O cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** define as configurações avançadas de proteção contra ameaças em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="339a9-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="339a9-107">Para habilitar a proteção avançada contra ameaças em um banco de dados, é necessário habilitar configurações de auditoria nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="339a9-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="339a9-108">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* , *nome_do_servidor* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="339a9-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="339a9-109">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="339a9-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="339a9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="339a9-110">EXAMPLES</span></span>

### <span data-ttu-id="339a9-111">Exemplo 1: definir as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="339a9-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="339a9-112">Esse comando define as configurações avançadas de proteção contra ameaças para um banco de dados denominado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="339a9-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="339a9-113">OS</span><span class="sxs-lookup"><span data-stu-id="339a9-113">PARAMETERS</span></span>

### <span data-ttu-id="339a9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="339a9-114">-DatabaseName</span></span>
<span data-ttu-id="339a9-115">Especifica o nome do banco de dados onde as configurações estão definidas.</span><span class="sxs-lookup"><span data-stu-id="339a9-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="339a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339a9-116">-DefaultProfile</span></span>
<span data-ttu-id="339a9-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="339a9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="339a9-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="339a9-118">-EmailAdmins</span></span>
<span data-ttu-id="339a9-119">Especifica se as configurações avançadas de proteção contra ameaças contatam os administradores usando o email.</span><span class="sxs-lookup"><span data-stu-id="339a9-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="339a9-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="339a9-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="339a9-121">Especifica uma matriz de tipos de detecção a serem excluídos das configurações.</span><span class="sxs-lookup"><span data-stu-id="339a9-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="339a9-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="339a9-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="339a9-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="339a9-123">Sql_Injection</span></span> 
- <span data-ttu-id="339a9-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="339a9-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="339a9-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="339a9-125">Access_Anomaly</span></span> 
- <span data-ttu-id="339a9-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="339a9-126">None</span></span>

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

### <span data-ttu-id="339a9-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="339a9-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="339a9-128">Especifica uma lista separada por ponto-e-vírgula de endereços de email aos quais as configurações enviam alertas.</span><span class="sxs-lookup"><span data-stu-id="339a9-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="339a9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="339a9-129">-PassThru</span></span>
<span data-ttu-id="339a9-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="339a9-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="339a9-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="339a9-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="339a9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339a9-132">-ResourceGroupName</span></span>
<span data-ttu-id="339a9-133">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="339a9-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="339a9-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="339a9-134">-RetentionInDays</span></span>
<span data-ttu-id="339a9-135">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="339a9-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="339a9-136">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="339a9-136">-ServerName</span></span>
<span data-ttu-id="339a9-137">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="339a9-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="339a9-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="339a9-138">-StorageAccountName</span></span>
<span data-ttu-id="339a9-139">Especifica o nome da conta de armazenamento a ser usada.</span><span class="sxs-lookup"><span data-stu-id="339a9-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="339a9-140">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="339a9-140">Wildcards are not permitted.</span></span> <span data-ttu-id="339a9-141">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="339a9-141">This parameter is not required.</span></span> <span data-ttu-id="339a9-142">Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte das configurações avançadas de proteção contra ameaças do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="339a9-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="339a9-143">Se esta for a primeira vez em que um banco de dados configurações avançadas de proteção contra ameaças estiver definido e esse parâmetro não for fornecido, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="339a9-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="339a9-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="339a9-144">-Confirm</span></span>
<span data-ttu-id="339a9-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="339a9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339a9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339a9-146">-WhatIf</span></span>
<span data-ttu-id="339a9-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="339a9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339a9-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="339a9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339a9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339a9-149">CommonParameters</span></span>
<span data-ttu-id="339a9-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339a9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339a9-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="339a9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339a9-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="339a9-152">INPUTS</span></span>

### <span data-ttu-id="339a9-153">System. String</span><span class="sxs-lookup"><span data-stu-id="339a9-153">System.String</span></span>

### <span data-ttu-id="339a9-154">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="339a9-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="339a9-155">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. detecttype []</span><span class="sxs-lookup"><span data-stu-id="339a9-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="339a9-156">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="339a9-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="339a9-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="339a9-157">OUTPUTS</span></span>

### <span data-ttu-id="339a9-158">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="339a9-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="339a9-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="339a9-159">NOTES</span></span>

## <span data-ttu-id="339a9-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="339a9-160">RELATED LINKS</span></span>

[<span data-ttu-id="339a9-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="339a9-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="339a9-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="339a9-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="339a9-163">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="339a9-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


