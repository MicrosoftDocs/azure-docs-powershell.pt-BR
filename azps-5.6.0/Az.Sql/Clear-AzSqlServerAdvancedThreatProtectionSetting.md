---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4a576c930d8ff1c53c6c9e92c7d87664aef4da4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893102"
---
# <span data-ttu-id="5e8c7-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="5e8c7-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="5e8c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8c7-103">Remove as configurações avançadas de proteção contra ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="5e8c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5e8c7-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e8c7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5e8c7-105">DESCRIPTION</span></span>
<span data-ttu-id="5e8c7-106">O Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet remove as configurações avançadas de proteção contra ameaças de um servidor SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="5e8c7-107">Para usar esse cmdlet, especifique os parâmetros ResourceGroupName e ServerName para identificar o servidor do qual esse cmdlet remove as configurações.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="5e8c7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e8c7-108">EXAMPLES</span></span>

### <span data-ttu-id="5e8c7-109">Exemplo 1: Remover configurações avançadas de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="5e8c7-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="5e8c7-110">Este comando remove as configurações avançadas de proteção contra ameaças de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="5e8c7-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5e8c7-111">PARAMETERS</span></span>

### <span data-ttu-id="5e8c7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8c7-112">-DefaultProfile</span></span>
<span data-ttu-id="5e8c7-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5e8c7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e8c7-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e8c7-114">-PassThru</span></span>
<span data-ttu-id="5e8c7-115">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5e8c7-116">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e8c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e8c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e8c7-118">Especifica o nome do grupo de recursos ao que o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="5e8c7-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e8c7-119">-ServerName</span></span>
<span data-ttu-id="5e8c7-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="5e8c7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e8c7-121">-Confirm</span></span>
<span data-ttu-id="5e8c7-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e8c7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e8c7-123">-WhatIf</span></span>
<span data-ttu-id="5e8c7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e8c7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e8c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8c7-126">CommonParameters</span></span>
<span data-ttu-id="5e8c7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8c7-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e8c7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8c7-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e8c7-129">INPUTS</span></span>

### <span data-ttu-id="5e8c7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5e8c7-130">System.String</span></span>

## <span data-ttu-id="5e8c7-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5e8c7-131">OUTPUTS</span></span>

### <span data-ttu-id="5e8c7-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="5e8c7-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="5e8c7-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="5e8c7-133">NOTES</span></span>

## <span data-ttu-id="5e8c7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e8c7-134">RELATED LINKS</span></span>

[<span data-ttu-id="5e8c7-135">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="5e8c7-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

