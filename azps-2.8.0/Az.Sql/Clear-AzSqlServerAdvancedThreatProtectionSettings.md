---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 215ab742a91bc70c51860950acedb3449966bda2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772382"
---
# <span data-ttu-id="ea845-101">Clear-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="ea845-101">Clear-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="ea845-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea845-102">SYNOPSIS</span></span>
<span data-ttu-id="ea845-103">Remove as configurações avançadas de proteção contra ameaças de um servidor.</span><span class="sxs-lookup"><span data-stu-id="ea845-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="ea845-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea845-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea845-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea845-105">DESCRIPTION</span></span>
<span data-ttu-id="ea845-106">O cmdlet Clear-AzSqlServerAdvancedThreatProtectionSettings remove as configurações avançadas de proteção contra ameaças de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea845-106">The Clear-AzSqlServerAdvancedThreatProtectionSettings cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="ea845-107">Para usar esse cmdlet, especifique os parâmetros ResourceGroupName e nomedoservidor para identificar o servidor do qual esse cmdlet Remove as configurações.</span><span class="sxs-lookup"><span data-stu-id="ea845-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="ea845-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea845-108">EXAMPLES</span></span>

### <span data-ttu-id="ea845-109">Exemplo 1: remover as configurações avançadas de proteção contra ameaças de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="ea845-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="ea845-110">Esse comando remove as configurações avançadas de proteção contra ameaças de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="ea845-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="ea845-111">OS</span><span class="sxs-lookup"><span data-stu-id="ea845-111">PARAMETERS</span></span>

### <span data-ttu-id="ea845-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea845-112">-DefaultProfile</span></span>
<span data-ttu-id="ea845-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ea845-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea845-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea845-114">-PassThru</span></span>
<span data-ttu-id="ea845-115">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ea845-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea845-116">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ea845-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea845-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea845-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea845-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="ea845-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="ea845-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ea845-119">-ServerName</span></span>
<span data-ttu-id="ea845-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="ea845-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="ea845-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea845-121">-Confirm</span></span>
<span data-ttu-id="ea845-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea845-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea845-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea845-123">-WhatIf</span></span>
<span data-ttu-id="ea845-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea845-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea845-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea845-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea845-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea845-126">CommonParameters</span></span>
<span data-ttu-id="ea845-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea845-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea845-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea845-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea845-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea845-129">INPUTS</span></span>

### <span data-ttu-id="ea845-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ea845-130">System.String</span></span>

## <span data-ttu-id="ea845-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea845-131">OUTPUTS</span></span>

### <span data-ttu-id="ea845-132">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="ea845-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="ea845-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea845-133">NOTES</span></span>

## <span data-ttu-id="ea845-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea845-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea845-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ea845-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

