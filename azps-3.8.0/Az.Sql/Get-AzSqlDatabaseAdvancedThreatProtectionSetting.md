---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941566"
---
# <span data-ttu-id="fed47-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="fed47-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="fed47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fed47-102">SYNOPSIS</span></span>
<span data-ttu-id="fed47-103">Obtém as configurações avançadas de proteção contra ameaças para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fed47-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="fed47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fed47-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fed47-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fed47-105">DESCRIPTION</span></span>
<span data-ttu-id="fed47-106">O cmdlet **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** Obtém as configurações avançadas de proteção contra ameaças de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fed47-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="fed47-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="fed47-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="fed47-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fed47-108">EXAMPLES</span></span>

### <span data-ttu-id="fed47-109">Exemplo 1: obter as configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="fed47-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="fed47-110">Este comando obtém as configurações avançadas de proteção contra ameaças para um banco de dados denominado Database01.</span><span class="sxs-lookup"><span data-stu-id="fed47-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="fed47-111">O banco de dados está localizado no servidor chamado Server01, que é atribuído à ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fed47-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="fed47-112">OS</span><span class="sxs-lookup"><span data-stu-id="fed47-112">PARAMETERS</span></span>

### <span data-ttu-id="fed47-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fed47-113">-DatabaseName</span></span>
<span data-ttu-id="fed47-114">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fed47-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="fed47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed47-115">-DefaultProfile</span></span>
<span data-ttu-id="fed47-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fed47-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fed47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed47-117">-ResourceGroupName</span></span>
<span data-ttu-id="fed47-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fed47-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fed47-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fed47-119">-ServerName</span></span>
<span data-ttu-id="fed47-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="fed47-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="fed47-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fed47-121">-Confirm</span></span>
<span data-ttu-id="fed47-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fed47-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed47-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fed47-123">-WhatIf</span></span>
<span data-ttu-id="fed47-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fed47-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fed47-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fed47-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fed47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed47-126">CommonParameters</span></span>
<span data-ttu-id="fed47-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed47-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fed47-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed47-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fed47-129">INPUTS</span></span>

### <span data-ttu-id="fed47-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fed47-130">System.String</span></span>

## <span data-ttu-id="fed47-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fed47-131">OUTPUTS</span></span>

### <span data-ttu-id="fed47-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="fed47-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="fed47-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fed47-133">NOTES</span></span>

## <span data-ttu-id="fed47-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fed47-134">RELATED LINKS</span></span>

[<span data-ttu-id="fed47-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="fed47-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



