---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 705412a560c4d4c0734e8e81a07fb2a85224f8c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887852"
---
# <span data-ttu-id="f9d23-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f9d23-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f9d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d23-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d23-103">Obtém as configurações avançadas de proteção contra ameaças para um servidor.</span><span class="sxs-lookup"><span data-stu-id="f9d23-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="f9d23-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f9d23-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d23-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f9d23-105">DESCRIPTION</span></span>
<span data-ttu-id="f9d23-106">O cmdlet **Get-AzSqlServerAdvancedThreatProtectionSetting** obtém as configurações avançadas de proteção contra ameaças de um servidor do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f9d23-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="f9d23-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="f9d23-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="f9d23-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9d23-108">EXAMPLES</span></span>

### <span data-ttu-id="f9d23-109">Exemplo 1: Obter as configurações avançadas de proteção contra ameaças para um servidor</span><span class="sxs-lookup"><span data-stu-id="f9d23-109">Example 1: Get the advanced threat protection settings for a server</span></span>
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

<span data-ttu-id="f9d23-110">Este comando obtém as configurações avançadas de proteção contra ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="f9d23-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="f9d23-111">O servidor é atribuído ao grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f9d23-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f9d23-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f9d23-112">PARAMETERS</span></span>

### <span data-ttu-id="f9d23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d23-113">-DefaultProfile</span></span>
<span data-ttu-id="f9d23-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f9d23-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9d23-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d23-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9d23-116">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="f9d23-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="f9d23-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9d23-117">-ServerName</span></span>
<span data-ttu-id="f9d23-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f9d23-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f9d23-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9d23-119">-Confirm</span></span>
<span data-ttu-id="f9d23-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d23-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d23-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d23-121">-WhatIf</span></span>
<span data-ttu-id="f9d23-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9d23-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d23-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9d23-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d23-124">CommonParameters</span></span>
<span data-ttu-id="f9d23-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d23-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9d23-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d23-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9d23-127">INPUTS</span></span>

### <span data-ttu-id="f9d23-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f9d23-128">System.String</span></span>

## <span data-ttu-id="f9d23-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f9d23-129">OUTPUTS</span></span>

### <span data-ttu-id="f9d23-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="f9d23-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="f9d23-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="f9d23-131">NOTES</span></span>

## <span data-ttu-id="f9d23-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9d23-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9d23-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f9d23-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="f9d23-134">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f9d23-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


