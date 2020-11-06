---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429032"
---
# <span data-ttu-id="7828b-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7828b-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="7828b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7828b-102">SYNOPSIS</span></span>
<span data-ttu-id="7828b-103">Define uma política de detecção de ameaças em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7828b-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7828b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7828b-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7828b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7828b-105">DESCRIPTION</span></span>
<span data-ttu-id="7828b-106">O cmdlet **set-AzureRmSqlDatabaseThreatDetectionPolicy** define uma política de detecção de ameaças em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7828b-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="7828b-107">Para habilitar a detecção de ameaças em um banco de dados, uma política de auditoria deve estar habilitada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7828b-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="7828b-108">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* , *nome_do_servidor* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7828b-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="7828b-109">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="7828b-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7828b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7828b-110">EXAMPLES</span></span>

### <span data-ttu-id="7828b-111">Exemplo 1: definir a política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="7828b-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="7828b-112">Esse comando define a política de detecção de ameaças para um banco de dados denominado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="7828b-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="7828b-113">OS</span><span class="sxs-lookup"><span data-stu-id="7828b-113">PARAMETERS</span></span>

### <span data-ttu-id="7828b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7828b-114">-DatabaseName</span></span>
<span data-ttu-id="7828b-115">Especifica o nome do banco de dados onde a política está definida.</span><span class="sxs-lookup"><span data-stu-id="7828b-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="7828b-116">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7828b-116">-EmailAdmins</span></span>
<span data-ttu-id="7828b-117">Especifica se a política de detecção de ameaças entra em contato com administradores por email.</span><span class="sxs-lookup"><span data-stu-id="7828b-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="7828b-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="7828b-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="7828b-119">Especifica uma matriz de tipos de detecção a serem excluídos da política.</span><span class="sxs-lookup"><span data-stu-id="7828b-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="7828b-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7828b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7828b-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="7828b-121">Sql_Injection</span></span> 
- <span data-ttu-id="7828b-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="7828b-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="7828b-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="7828b-123">Access_Anomaly</span></span> 
- <span data-ttu-id="7828b-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7828b-124">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7828b-125">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="7828b-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="7828b-126">Especifica uma lista separada por ponto-e-vírgula de endereços de email aos quais a política envia alertas.</span><span class="sxs-lookup"><span data-stu-id="7828b-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="7828b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7828b-127">-PassThru</span></span>
<span data-ttu-id="7828b-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="7828b-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7828b-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7828b-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7828b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7828b-130">-ResourceGroupName</span></span>
<span data-ttu-id="7828b-131">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7828b-131">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7828b-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7828b-132">-RetentionInDays</span></span>
<span data-ttu-id="7828b-133">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="7828b-133">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="7828b-134">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7828b-134">-ServerName</span></span>
<span data-ttu-id="7828b-135">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="7828b-135">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7828b-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7828b-136">-StorageAccountName</span></span>
<span data-ttu-id="7828b-137">Especifica o nome da conta de armazenamento a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7828b-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="7828b-138">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="7828b-138">Wildcards are not permitted.</span></span> <span data-ttu-id="7828b-139">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="7828b-139">This parameter is not required.</span></span> <span data-ttu-id="7828b-140">Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte da política de detecção de ameaças do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7828b-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="7828b-141">Se esta for a primeira vez que uma política de detecção de ameaças de banco de dados for definida e esse parâmetro não for fornecido, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="7828b-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="7828b-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7828b-142">-Confirm</span></span>
<span data-ttu-id="7828b-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7828b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7828b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7828b-144">-WhatIf</span></span>
<span data-ttu-id="7828b-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7828b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7828b-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7828b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7828b-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7828b-147">-DefaultProfile</span></span>
<span data-ttu-id="7828b-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7828b-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7828b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7828b-149">CommonParameters</span></span>
<span data-ttu-id="7828b-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7828b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7828b-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7828b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7828b-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7828b-152">INPUTS</span></span>

###  
<span data-ttu-id="7828b-153">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7828b-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="7828b-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7828b-154">OUTPUTS</span></span>

### <span data-ttu-id="7828b-155">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7828b-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="7828b-156">Esse cmdlet retorna um objeto **Model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="7828b-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="7828b-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7828b-157">NOTES</span></span>

## <span data-ttu-id="7828b-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7828b-158">RELATED LINKS</span></span>

[<span data-ttu-id="7828b-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7828b-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="7828b-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7828b-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="7828b-161">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7828b-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


