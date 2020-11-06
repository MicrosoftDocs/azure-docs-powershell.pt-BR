---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441365"
---
# <span data-ttu-id="08eae-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08eae-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="08eae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08eae-102">SYNOPSIS</span></span>
<span data-ttu-id="08eae-103">Define uma política de detecção de ameaças em um servidor.</span><span class="sxs-lookup"><span data-stu-id="08eae-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08eae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08eae-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08eae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08eae-105">DESCRIPTION</span></span>
<span data-ttu-id="08eae-106">O cmdlet **set-AzureRmSqlServerThreatDetectionPolicy** define uma política de detecção de ameaças em um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="08eae-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="08eae-107">Para habilitar a detecção de ameaças em um servidor, uma política de auditoria deve estar habilitada nesse servidor.</span><span class="sxs-lookup"><span data-stu-id="08eae-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="08eae-108">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e ServerName para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="08eae-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="08eae-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08eae-109">EXAMPLES</span></span>

### <span data-ttu-id="08eae-110">Exemplo 1: definir a política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="08eae-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="08eae-111">Este comando define a política de detecção de ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="08eae-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="08eae-112">OS</span><span class="sxs-lookup"><span data-stu-id="08eae-112">PARAMETERS</span></span>

### <span data-ttu-id="08eae-113">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="08eae-113">-EmailAdmins</span></span>
<span data-ttu-id="08eae-114">Especifica se a política de detecção de ameaças entra em contato com administradores por email.</span><span class="sxs-lookup"><span data-stu-id="08eae-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="08eae-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="08eae-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="08eae-116">Especifica uma matriz de tipos de detecção a serem excluídos da política.</span><span class="sxs-lookup"><span data-stu-id="08eae-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="08eae-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08eae-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08eae-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="08eae-118">Sql_Injection</span></span>
- <span data-ttu-id="08eae-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="08eae-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="08eae-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="08eae-120">Access_Anomaly</span></span>
- <span data-ttu-id="08eae-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="08eae-121">None</span></span>

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

### <span data-ttu-id="08eae-122">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="08eae-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="08eae-123">Especifica uma lista separada por ponto-e-vírgula de endereços de email aos quais a política envia alertas.</span><span class="sxs-lookup"><span data-stu-id="08eae-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="08eae-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08eae-124">-PassThru</span></span>
<span data-ttu-id="08eae-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="08eae-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="08eae-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="08eae-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08eae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08eae-127">-ResourceGroupName</span></span>
<span data-ttu-id="08eae-128">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="08eae-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="08eae-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="08eae-129">-RetentionInDays</span></span>
<span data-ttu-id="08eae-130">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="08eae-130">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="08eae-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="08eae-131">-ServerName</span></span>
<span data-ttu-id="08eae-132">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="08eae-132">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="08eae-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="08eae-133">-StorageAccountName</span></span>
<span data-ttu-id="08eae-134">Especifica o nome da conta de armazenamento a ser usada.</span><span class="sxs-lookup"><span data-stu-id="08eae-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="08eae-135">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="08eae-135">Wildcards are not permitted.</span></span> <span data-ttu-id="08eae-136">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="08eae-136">This parameter is not required.</span></span> <span data-ttu-id="08eae-137">Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte da política de detecção de ameaças do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08eae-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="08eae-138">Se esta for a primeira vez que uma política de detecção do banco de dados do theat é definida e esse parâmetro não for fornecido, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="08eae-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="08eae-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08eae-139">-Confirm</span></span>
<span data-ttu-id="08eae-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08eae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08eae-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08eae-141">-WhatIf</span></span>
<span data-ttu-id="08eae-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08eae-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08eae-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08eae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08eae-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08eae-144">-DefaultProfile</span></span>
<span data-ttu-id="08eae-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08eae-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08eae-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08eae-146">CommonParameters</span></span>
<span data-ttu-id="08eae-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08eae-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08eae-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08eae-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08eae-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08eae-149">INPUTS</span></span>

###  
<span data-ttu-id="08eae-150">Não é possível canalizar a entrada para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08eae-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="08eae-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08eae-151">OUTPUTS</span></span>

### <span data-ttu-id="08eae-152">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="08eae-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="08eae-153">Esse cmdlet retorna um objeto **ServerThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="08eae-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="08eae-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08eae-154">NOTES</span></span>

## <span data-ttu-id="08eae-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08eae-155">RELATED LINKS</span></span>

[<span data-ttu-id="08eae-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08eae-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="08eae-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08eae-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="08eae-158">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="08eae-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)