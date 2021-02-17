---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 49b484c17b595a8f676a089f8627b70a1f34c471
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399491"
---
# <span data-ttu-id="62dbd-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="62dbd-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="62dbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="62dbd-103">Define uma política de detecção de ameaças em um servidor.</span><span class="sxs-lookup"><span data-stu-id="62dbd-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="62dbd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62dbd-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62dbd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="62dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="62dbd-106">O cmdlet **Set-AzSqlServerThreatDetectionPolicy** define uma política de detecção de ameaças em um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="62dbd-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="62dbd-107">Para habilitar a detecção de ameaças em um servidor, uma política de auditoria deve ser habilitada nesse servidor.</span><span class="sxs-lookup"><span data-stu-id="62dbd-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="62dbd-108">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e ServerName para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="62dbd-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="62dbd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62dbd-109">EXAMPLES</span></span>

### <span data-ttu-id="62dbd-110">Exemplo 1: Definir a política de detecção de ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="62dbd-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="62dbd-111">Esse comando define a política de detecção de ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="62dbd-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="62dbd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62dbd-112">PARAMETERS</span></span>

### <span data-ttu-id="62dbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62dbd-113">-DefaultProfile</span></span>
<span data-ttu-id="62dbd-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="62dbd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62dbd-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="62dbd-115">-EmailAdmins</span></span>
<span data-ttu-id="62dbd-116">Especifica se a política de detecção de ameaças contata os administradores usando o email.</span><span class="sxs-lookup"><span data-stu-id="62dbd-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="62dbd-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="62dbd-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="62dbd-118">Especifica uma matriz de tipos de detecção a ser excluída da política.</span><span class="sxs-lookup"><span data-stu-id="62dbd-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="62dbd-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="62dbd-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62dbd-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="62dbd-120">Sql_Injection</span></span>
- <span data-ttu-id="62dbd-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="62dbd-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="62dbd-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="62dbd-122">Access_Anomaly</span></span>
- <span data-ttu-id="62dbd-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="62dbd-123">None</span></span>

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

### <span data-ttu-id="62dbd-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="62dbd-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="62dbd-125">Especifica uma lista separada por ponto e vírgula dos endereços de email para os quais a política envia alertas.</span><span class="sxs-lookup"><span data-stu-id="62dbd-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="62dbd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62dbd-126">-PassThru</span></span>
<span data-ttu-id="62dbd-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="62dbd-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="62dbd-128">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="62dbd-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="62dbd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62dbd-129">-ResourceGroupName</span></span>
<span data-ttu-id="62dbd-130">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="62dbd-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="62dbd-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="62dbd-131">-RetentionInDays</span></span>
<span data-ttu-id="62dbd-132">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="62dbd-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="62dbd-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62dbd-133">-ServerName</span></span>
<span data-ttu-id="62dbd-134">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="62dbd-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="62dbd-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62dbd-135">-StorageAccountName</span></span>
<span data-ttu-id="62dbd-136">Especifica o nome da conta de armazenamento a ser usada.</span><span class="sxs-lookup"><span data-stu-id="62dbd-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="62dbd-137">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="62dbd-137">Wildcards are not permitted.</span></span> <span data-ttu-id="62dbd-138">Este parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="62dbd-138">This parameter is not required.</span></span> <span data-ttu-id="62dbd-139">Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte da política de detecção de ameaças do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="62dbd-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="62dbd-140">Se esta for a primeira vez que uma política de detecção de banco de dados theat é definida e esse parâmetro não é fornecido, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="62dbd-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="62dbd-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="62dbd-141">-Confirm</span></span>
<span data-ttu-id="62dbd-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62dbd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62dbd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62dbd-143">-WhatIf</span></span>
<span data-ttu-id="62dbd-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="62dbd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62dbd-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62dbd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62dbd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62dbd-146">CommonParameters</span></span>
<span data-ttu-id="62dbd-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62dbd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62dbd-148">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62dbd-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62dbd-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="62dbd-149">INPUTS</span></span>

### <span data-ttu-id="62dbd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="62dbd-150">System.String</span></span>

### <span data-ttu-id="62dbd-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62dbd-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="62dbd-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="62dbd-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="62dbd-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62dbd-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="62dbd-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="62dbd-154">OUTPUTS</span></span>

### <span data-ttu-id="62dbd-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="62dbd-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="62dbd-156">Notas</span><span class="sxs-lookup"><span data-stu-id="62dbd-156">NOTES</span></span>

## <span data-ttu-id="62dbd-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62dbd-157">RELATED LINKS</span></span>

[<span data-ttu-id="62dbd-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="62dbd-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="62dbd-159">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="62dbd-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
