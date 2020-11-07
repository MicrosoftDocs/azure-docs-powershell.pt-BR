---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: f15ccf5c397ece13a034c99c29ac6cd5f18f9f58
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773166"
---
# <span data-ttu-id="196af-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="196af-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="196af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="196af-102">SYNOPSIS</span></span>
<span data-ttu-id="196af-103">Remove as configurações avançadas de proteção contra ameaças de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="196af-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="196af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="196af-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="196af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="196af-105">DESCRIPTION</span></span>
<span data-ttu-id="196af-106">O cmdlet **Clear-AzSqlDatabaseAdvancedThreatProtectionSettings** remove as configurações avançadas de proteção contra ameaças de um banco de dados SQL do AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="196af-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="196af-107">Para usar esse cmdlet, especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o banco de dados do qual esse cmdlet Remove as configurações.</span><span class="sxs-lookup"><span data-stu-id="196af-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="196af-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="196af-108">EXAMPLES</span></span>

### <span data-ttu-id="196af-109">Exemplo 1: remover as configurações avançadas de proteção contra ameaças de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="196af-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="196af-110">Esse comando remove as configurações avançadas de proteção contra ameaças de um banco de dados denominado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="196af-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="196af-111">OS</span><span class="sxs-lookup"><span data-stu-id="196af-111">PARAMETERS</span></span>

### <span data-ttu-id="196af-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="196af-112">-DatabaseName</span></span>
<span data-ttu-id="196af-113">Especifica o nome de um banco de dados onde as configurações avançadas de proteção contra ameaças devem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="196af-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="196af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196af-114">-DefaultProfile</span></span>
<span data-ttu-id="196af-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="196af-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="196af-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="196af-116">-PassThru</span></span>
<span data-ttu-id="196af-117">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="196af-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="196af-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="196af-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="196af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196af-119">-ResourceGroupName</span></span>
<span data-ttu-id="196af-120">Especifica o nome do grupo de recursos que o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="196af-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="196af-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="196af-121">-ServerName</span></span>
<span data-ttu-id="196af-122">Especifica o nome de um servidor no qual o banco de dados é executado.</span><span class="sxs-lookup"><span data-stu-id="196af-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="196af-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="196af-123">-Confirm</span></span>
<span data-ttu-id="196af-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196af-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196af-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196af-125">-WhatIf</span></span>
<span data-ttu-id="196af-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="196af-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="196af-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="196af-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196af-128">CommonParameters</span></span>
<span data-ttu-id="196af-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196af-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="196af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196af-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="196af-131">INPUTS</span></span>

### <span data-ttu-id="196af-132">System. String</span><span class="sxs-lookup"><span data-stu-id="196af-132">System.String</span></span>

## <span data-ttu-id="196af-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="196af-133">OUTPUTS</span></span>

### <span data-ttu-id="196af-134">Microsoft. Azure. Commands. Sql. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="196af-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="196af-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="196af-135">NOTES</span></span>

## <span data-ttu-id="196af-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="196af-136">RELATED LINKS</span></span>

[<span data-ttu-id="196af-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="196af-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


