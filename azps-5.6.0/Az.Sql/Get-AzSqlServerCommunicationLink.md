---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 20f0fe00486b6b81ec1600e518c42121f5369095
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889145"
---
# <span data-ttu-id="35374-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="35374-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="35374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35374-102">SYNOPSIS</span></span>
<span data-ttu-id="35374-103">Obtém links de comunicação para transações de banco de dados elásticas entre servidores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35374-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="35374-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="35374-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35374-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="35374-105">DESCRIPTION</span></span>
<span data-ttu-id="35374-106">O cmdlet **Get-AzSqlServerCommunicationLink obtém** links de comunicação de servidor para servidor para transações de banco de dados elásticas no Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="35374-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="35374-107">Especifique o nome de um link de comunicação do servidor para ver as propriedades desse link.</span><span class="sxs-lookup"><span data-stu-id="35374-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="35374-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35374-108">EXAMPLES</span></span>

### <span data-ttu-id="35374-109">Exemplo 1: Obter todos os links de comunicação para um servidor</span><span class="sxs-lookup"><span data-stu-id="35374-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="35374-110">Este comando obtém todos os links de comunicação de servidor para servidor para transações de banco de dados elásticas para o servidor chamado ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="35374-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="35374-111">Exemplo 2: Obter um link de comunicação específico para um servidor</span><span class="sxs-lookup"><span data-stu-id="35374-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="35374-112">Este comando obtém o link de comunicação servidor para servidor chamado Link01.</span><span class="sxs-lookup"><span data-stu-id="35374-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="35374-113">Exemplo 3: Obter todos os links de comunicação para um servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="35374-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="35374-114">Este comando obtém todos os links de comunicação de servidor para servidor para transações de banco de dados elásticas para o servidor chamado ContosoServer17 que começam com "Link".</span><span class="sxs-lookup"><span data-stu-id="35374-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="35374-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="35374-115">PARAMETERS</span></span>

### <span data-ttu-id="35374-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35374-116">-DefaultProfile</span></span>
<span data-ttu-id="35374-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="35374-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35374-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="35374-118">-LinkName</span></span>
<span data-ttu-id="35374-119">Especifica o nome do link de comunicação do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="35374-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35374-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35374-120">-ResourceGroupName</span></span>
<span data-ttu-id="35374-121">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo *parâmetro ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="35374-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="35374-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="35374-122">-ServerName</span></span>
<span data-ttu-id="35374-123">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="35374-123">Specifies the name of a server.</span></span>
<span data-ttu-id="35374-124">Este servidor contém um link de comunicação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="35374-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="35374-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35374-125">-Confirm</span></span>
<span data-ttu-id="35374-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35374-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35374-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35374-127">-WhatIf</span></span>
<span data-ttu-id="35374-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35374-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35374-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35374-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35374-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35374-130">CommonParameters</span></span>
<span data-ttu-id="35374-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35374-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35374-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35374-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35374-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35374-133">INPUTS</span></span>

### <span data-ttu-id="35374-134">System.String</span><span class="sxs-lookup"><span data-stu-id="35374-134">System.String</span></span>

## <span data-ttu-id="35374-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="35374-135">OUTPUTS</span></span>

### <span data-ttu-id="35374-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="35374-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="35374-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="35374-137">NOTES</span></span>
* <span data-ttu-id="35374-138">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="35374-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="35374-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35374-139">RELATED LINKS</span></span>

[<span data-ttu-id="35374-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="35374-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="35374-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="35374-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="35374-142">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="35374-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
