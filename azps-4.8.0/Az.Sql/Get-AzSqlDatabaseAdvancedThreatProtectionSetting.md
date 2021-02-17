---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9035f2a03ac04a9bc99248c48675ab3c69b84207
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415352"
---
# <span data-ttu-id="3bc1d-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3bc1d-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3bc1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3bc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc1d-103">Obtém as configurações avançadas de proteção contra ameaças para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="3bc1d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bc1d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bc1d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bc1d-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc1d-106">O cmdlet **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** obtém as configurações avançadas de proteção contra ameaças de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="3bc1d-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="3bc1d-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3bc1d-108">EXAMPLES</span></span>

### <span data-ttu-id="3bc1d-109">Exemplo 1: Obter as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="3bc1d-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="3bc1d-110">Esse comando obtém as configurações avançadas de proteção contra ameaças para um banco de dados chamado Banco de Dados01.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="3bc1d-111">O banco de dados está localizado no servidor chamado Server01, que é atribuído ao grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="3bc1d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bc1d-112">PARAMETERS</span></span>

### <span data-ttu-id="3bc1d-113">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="3bc1d-113">-DatabaseName</span></span>
<span data-ttu-id="3bc1d-114">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="3bc1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc1d-115">-DefaultProfile</span></span>
<span data-ttu-id="3bc1d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3bc1d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bc1d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc1d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3bc1d-118">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3bc1d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3bc1d-119">-ServerName</span></span>
<span data-ttu-id="3bc1d-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="3bc1d-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3bc1d-121">-Confirm</span></span>
<span data-ttu-id="3bc1d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc1d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc1d-123">-WhatIf</span></span>
<span data-ttu-id="3bc1d-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc1d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc1d-126">CommonParameters</span></span>
<span data-ttu-id="3bc1d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc1d-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bc1d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc1d-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="3bc1d-129">INPUTS</span></span>

### <span data-ttu-id="3bc1d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3bc1d-130">System.String</span></span>

## <span data-ttu-id="3bc1d-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="3bc1d-131">OUTPUTS</span></span>

### <span data-ttu-id="3bc1d-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="3bc1d-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="3bc1d-133">Notas</span><span class="sxs-lookup"><span data-stu-id="3bc1d-133">NOTES</span></span>

## <span data-ttu-id="3bc1d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bc1d-134">RELATED LINKS</span></span>




