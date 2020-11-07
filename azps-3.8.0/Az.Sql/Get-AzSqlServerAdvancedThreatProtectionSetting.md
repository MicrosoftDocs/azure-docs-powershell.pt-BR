---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940785"
---
# <span data-ttu-id="11e6a-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="11e6a-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="11e6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="11e6a-103">Obtém as configurações avançadas de proteção contra ameaças para um servidor.</span><span class="sxs-lookup"><span data-stu-id="11e6a-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="11e6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11e6a-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="11e6a-106">O cmdlet **Get-AzSqlServerAdvancedThreatProtectionSetting** Obtém as configurações avançadas de proteção contra ameaças de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="11e6a-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="11e6a-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="11e6a-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="11e6a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11e6a-108">EXAMPLES</span></span>

### <span data-ttu-id="11e6a-109">Exemplo 1: obter as configurações avançadas de proteção contra ameaças para um servidor</span><span class="sxs-lookup"><span data-stu-id="11e6a-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="11e6a-110">Este comando obtém as configurações avançadas de proteção contra ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="11e6a-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="11e6a-111">O servidor é atribuído à ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11e6a-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="11e6a-112">OS</span><span class="sxs-lookup"><span data-stu-id="11e6a-112">PARAMETERS</span></span>

### <span data-ttu-id="11e6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e6a-113">-DefaultProfile</span></span>
<span data-ttu-id="11e6a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="11e6a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11e6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="11e6a-116">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="11e6a-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="11e6a-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="11e6a-117">-ServerName</span></span>
<span data-ttu-id="11e6a-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="11e6a-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="11e6a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11e6a-119">-Confirm</span></span>
<span data-ttu-id="11e6a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11e6a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e6a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e6a-121">-WhatIf</span></span>
<span data-ttu-id="11e6a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11e6a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e6a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11e6a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e6a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e6a-124">CommonParameters</span></span>
<span data-ttu-id="11e6a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e6a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e6a-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11e6a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e6a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11e6a-127">INPUTS</span></span>

### <span data-ttu-id="11e6a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="11e6a-128">System.String</span></span>

## <span data-ttu-id="11e6a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11e6a-129">OUTPUTS</span></span>

### <span data-ttu-id="11e6a-130">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="11e6a-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="11e6a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11e6a-131">NOTES</span></span>

## <span data-ttu-id="11e6a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11e6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="11e6a-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="11e6a-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="11e6a-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="11e6a-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


