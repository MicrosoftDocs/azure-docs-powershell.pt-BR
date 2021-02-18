---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 38388f4a2d1d88ae668b8a6384ca228a9436ac68
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405900"
---
# <span data-ttu-id="efdd1-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="efdd1-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="efdd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efdd1-102">SYNOPSIS</span></span>
<span data-ttu-id="efdd1-103">Obtém as configurações avançadas de proteção contra ameaças para um servidor.</span><span class="sxs-lookup"><span data-stu-id="efdd1-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="efdd1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efdd1-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSettings -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efdd1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="efdd1-105">DESCRIPTION</span></span>
<span data-ttu-id="efdd1-106">O cmdlet **Get-AzSqlServerAdvancedThreatProtectionSettings** obtém as configurações avançadas de proteção contra ameaças de um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="efdd1-106">The **Get-AzSqlServerAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="efdd1-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor para o qual esse cmdlet obtém as configurações.</span><span class="sxs-lookup"><span data-stu-id="efdd1-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="efdd1-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="efdd1-108">EXAMPLES</span></span>

### <span data-ttu-id="efdd1-109">Exemplo 1: Obter as configurações avançadas de proteção contra ameaças para um servidor</span><span class="sxs-lookup"><span data-stu-id="efdd1-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="efdd1-110">Esse comando obtém as configurações avançadas de proteção contra ameaças para um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="efdd1-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="efdd1-111">O servidor é atribuído ao grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="efdd1-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="efdd1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efdd1-112">PARAMETERS</span></span>

### <span data-ttu-id="efdd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efdd1-113">-DefaultProfile</span></span>
<span data-ttu-id="efdd1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="efdd1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efdd1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efdd1-115">-ResourceGroupName</span></span>
<span data-ttu-id="efdd1-116">Especifica o nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="efdd1-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="efdd1-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="efdd1-117">-ServerName</span></span>
<span data-ttu-id="efdd1-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="efdd1-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="efdd1-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="efdd1-119">-Confirm</span></span>
<span data-ttu-id="efdd1-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efdd1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efdd1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efdd1-121">-WhatIf</span></span>
<span data-ttu-id="efdd1-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="efdd1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efdd1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efdd1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efdd1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efdd1-124">CommonParameters</span></span>
<span data-ttu-id="efdd1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efdd1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efdd1-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efdd1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efdd1-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="efdd1-127">INPUTS</span></span>

### <span data-ttu-id="efdd1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="efdd1-128">System.String</span></span>

## <span data-ttu-id="efdd1-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="efdd1-129">OUTPUTS</span></span>

### <span data-ttu-id="efdd1-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="efdd1-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="efdd1-131">Notas</span><span class="sxs-lookup"><span data-stu-id="efdd1-131">NOTES</span></span>

## <span data-ttu-id="efdd1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efdd1-132">RELATED LINKS</span></span>


[<span data-ttu-id="efdd1-133">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="efdd1-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


