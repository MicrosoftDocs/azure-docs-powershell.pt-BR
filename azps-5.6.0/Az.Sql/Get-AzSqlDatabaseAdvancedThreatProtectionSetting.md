---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 570b56ab98e8679a47bcb26b36f1bea4d24bd275
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890698"
---
# <span data-ttu-id="1488c-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1488c-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="1488c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1488c-102">SYNOPSIS</span></span>
<span data-ttu-id="1488c-103">Obtém as configurações avançadas de proteção contra ameaças para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1488c-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="1488c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1488c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1488c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1488c-105">DESCRIPTION</span></span>
<span data-ttu-id="1488c-106">O cmdlet **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** obtém as configurações avançadas de proteção contra ameaças de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1488c-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="1488c-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="1488c-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="1488c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1488c-108">EXAMPLES</span></span>

### <span data-ttu-id="1488c-109">Exemplo 1: Obter as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="1488c-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="1488c-110">Este comando obtém as configurações avançadas de proteção contra ameaças para um banco de dados chamado Database01.</span><span class="sxs-lookup"><span data-stu-id="1488c-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="1488c-111">O banco de dados está localizado no servidor chamado Server01, que é atribuído ao grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1488c-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1488c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1488c-112">PARAMETERS</span></span>

### <span data-ttu-id="1488c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1488c-113">-DatabaseName</span></span>
<span data-ttu-id="1488c-114">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1488c-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="1488c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1488c-115">-DefaultProfile</span></span>
<span data-ttu-id="1488c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1488c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1488c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1488c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1488c-118">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="1488c-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1488c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1488c-119">-ServerName</span></span>
<span data-ttu-id="1488c-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="1488c-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="1488c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1488c-121">-Confirm</span></span>
<span data-ttu-id="1488c-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1488c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1488c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1488c-123">-WhatIf</span></span>
<span data-ttu-id="1488c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1488c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1488c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1488c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1488c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1488c-126">CommonParameters</span></span>
<span data-ttu-id="1488c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1488c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1488c-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1488c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1488c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1488c-129">INPUTS</span></span>

### <span data-ttu-id="1488c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1488c-130">System.String</span></span>

## <span data-ttu-id="1488c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1488c-131">OUTPUTS</span></span>

### <span data-ttu-id="1488c-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="1488c-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="1488c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="1488c-133">NOTES</span></span>

## <span data-ttu-id="1488c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1488c-134">RELATED LINKS</span></span>

[<span data-ttu-id="1488c-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1488c-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



