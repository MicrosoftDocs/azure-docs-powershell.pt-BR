---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 186ff32138bba0556b05e9674f1711e9425a20c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773689"
---
# <span data-ttu-id="871fa-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="871fa-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="871fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="871fa-102">SYNOPSIS</span></span>
<span data-ttu-id="871fa-103">Obtém as configurações avançadas de proteção contra ameaças para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="871fa-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="871fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="871fa-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="871fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="871fa-105">DESCRIPTION</span></span>
<span data-ttu-id="871fa-106">O cmdlet **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** Obtém as configurações avançadas de proteção contra ameaças de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="871fa-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="871fa-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="871fa-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="871fa-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="871fa-108">EXAMPLES</span></span>

### <span data-ttu-id="871fa-109">Exemplo 1: obter as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="871fa-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="871fa-110">Este comando obtém as configurações avançadas de proteção contra ameaças para um banco de dados denominado Database01.</span><span class="sxs-lookup"><span data-stu-id="871fa-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="871fa-111">O banco de dados está localizado no servidor chamado Server01, que é atribuído à ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="871fa-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="871fa-112">OS</span><span class="sxs-lookup"><span data-stu-id="871fa-112">PARAMETERS</span></span>

### <span data-ttu-id="871fa-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="871fa-113">-DatabaseName</span></span>
<span data-ttu-id="871fa-114">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="871fa-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="871fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871fa-115">-DefaultProfile</span></span>
<span data-ttu-id="871fa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="871fa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="871fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="871fa-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="871fa-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="871fa-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="871fa-119">-ServerName</span></span>
<span data-ttu-id="871fa-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="871fa-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="871fa-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="871fa-121">-Confirm</span></span>
<span data-ttu-id="871fa-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="871fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="871fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="871fa-123">-WhatIf</span></span>
<span data-ttu-id="871fa-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="871fa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="871fa-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="871fa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="871fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871fa-126">CommonParameters</span></span>
<span data-ttu-id="871fa-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871fa-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="871fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871fa-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="871fa-129">INPUTS</span></span>

### <span data-ttu-id="871fa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="871fa-130">System.String</span></span>

## <span data-ttu-id="871fa-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="871fa-131">OUTPUTS</span></span>

### <span data-ttu-id="871fa-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="871fa-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="871fa-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="871fa-133">NOTES</span></span>

## <span data-ttu-id="871fa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="871fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="871fa-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="871fa-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)



