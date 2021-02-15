---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112542"
---
# <span data-ttu-id="e6f5f-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e6f5f-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e6f5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f5f-103">Obtém as configurações avançadas de proteção contra ameaças para um servidor.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="e6f5f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6f5f-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f5f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f5f-106">O cmdlet **Get-AzSqlServerAdvancedThreatProtectionSetting** obtém as configurações avançadas de proteção contra ameaças de um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="e6f5f-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="e6f5f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6f5f-108">EXAMPLES</span></span>

### <span data-ttu-id="e6f5f-109">Exemplo 1: Obter as configurações avançadas de proteção contra ameaças para um servidor</span><span class="sxs-lookup"><span data-stu-id="e6f5f-109">Example 1: Get the advanced threat protection settings for a server</span></span>
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

<span data-ttu-id="e6f5f-110">Esse comando obtém as configurações avançadas de proteção contra ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="e6f5f-111">O servidor é atribuído ao grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="e6f5f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6f5f-112">PARAMETERS</span></span>

### <span data-ttu-id="e6f5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f5f-113">-DefaultProfile</span></span>
<span data-ttu-id="e6f5f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e6f5f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6f5f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f5f-115">-ResourceGroupName</span></span>
<span data-ttu-id="e6f5f-116">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="e6f5f-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6f5f-117">-ServerName</span></span>
<span data-ttu-id="e6f5f-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e6f5f-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e6f5f-119">-Confirm</span></span>
<span data-ttu-id="e6f5f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f5f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f5f-121">-WhatIf</span></span>
<span data-ttu-id="e6f5f-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f5f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f5f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f5f-124">CommonParameters</span></span>
<span data-ttu-id="e6f5f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f5f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f5f-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6f5f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f5f-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="e6f5f-127">INPUTS</span></span>

### <span data-ttu-id="e6f5f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e6f5f-128">System.String</span></span>

## <span data-ttu-id="e6f5f-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="e6f5f-129">OUTPUTS</span></span>

### <span data-ttu-id="e6f5f-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="e6f5f-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="e6f5f-131">Notas</span><span class="sxs-lookup"><span data-stu-id="e6f5f-131">NOTES</span></span>

## <span data-ttu-id="e6f5f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6f5f-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6f5f-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e6f5f-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="e6f5f-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e6f5f-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


