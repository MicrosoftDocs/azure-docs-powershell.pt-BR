---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118614"
---
# <span data-ttu-id="b5298-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="b5298-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="b5298-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5298-102">SYNOPSIS</span></span>
<span data-ttu-id="b5298-103">Remove as configurações avançadas de proteção contra ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="b5298-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="b5298-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5298-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5298-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5298-105">DESCRIPTION</span></span>
<span data-ttu-id="b5298-106">O Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet remove as configurações avançadas de proteção contra ameaças de um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b5298-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="b5298-107">Para usar esse cmdlet, especifique os parâmetros ResourceGroupName e ServerName para identificar o servidor do qual esse cmdlet remove as configurações.</span><span class="sxs-lookup"><span data-stu-id="b5298-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="b5298-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5298-108">EXAMPLES</span></span>

### <span data-ttu-id="b5298-109">Exemplo 1: Remover uma configuração avançada de proteção contra ameaças para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="b5298-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="b5298-110">Esse comando remove as configurações avançadas de proteção contra ameaças de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="b5298-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="b5298-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5298-111">PARAMETERS</span></span>

### <span data-ttu-id="b5298-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5298-112">-DefaultProfile</span></span>
<span data-ttu-id="b5298-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b5298-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5298-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5298-114">-PassThru</span></span>
<span data-ttu-id="b5298-115">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b5298-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b5298-116">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="b5298-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5298-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5298-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5298-118">Especifica o nome do grupo de recursos ao que o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b5298-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="b5298-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5298-119">-ServerName</span></span>
<span data-ttu-id="b5298-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="b5298-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="b5298-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b5298-121">-Confirm</span></span>
<span data-ttu-id="b5298-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5298-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5298-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5298-123">-WhatIf</span></span>
<span data-ttu-id="b5298-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b5298-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5298-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5298-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5298-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5298-126">CommonParameters</span></span>
<span data-ttu-id="b5298-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5298-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5298-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5298-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5298-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b5298-129">INPUTS</span></span>

### <span data-ttu-id="b5298-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b5298-130">System.String</span></span>

## <span data-ttu-id="b5298-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="b5298-131">OUTPUTS</span></span>

### <span data-ttu-id="b5298-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="b5298-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="b5298-133">Notas</span><span class="sxs-lookup"><span data-stu-id="b5298-133">NOTES</span></span>

## <span data-ttu-id="b5298-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5298-134">RELATED LINKS</span></span>

[<span data-ttu-id="b5298-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b5298-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

