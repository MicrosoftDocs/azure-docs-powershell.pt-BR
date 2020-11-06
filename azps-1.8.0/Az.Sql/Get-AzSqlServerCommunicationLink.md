---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: b2d4d5e86870bf0c69e506f387f6309dbcc8af7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598947"
---
# <span data-ttu-id="78d65-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="78d65-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="78d65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78d65-102">SYNOPSIS</span></span>
<span data-ttu-id="78d65-103">Obtém links de comunicação para transações de banco de dados elástico entre servidores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="78d65-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="78d65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78d65-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d65-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78d65-105">DESCRIPTION</span></span>
<span data-ttu-id="78d65-106">O cmdlet **Get-AzSqlServerCommunicationLink** Obtém links de comunicação entre servidores para transações de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="78d65-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="78d65-107">Especifique o nome de um link de comunicação do servidor para ver as propriedades desse link.</span><span class="sxs-lookup"><span data-stu-id="78d65-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="78d65-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78d65-108">EXAMPLES</span></span>

### <span data-ttu-id="78d65-109">Exemplo 1: obter todos os links de comunicação para um servidor</span><span class="sxs-lookup"><span data-stu-id="78d65-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="78d65-110">Esse comando obtém todos os links de comunicação entre servidores para transações de banco de dados elástico para o servidor chamado ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="78d65-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="78d65-111">Exemplo 2: obter um link de comunicação específico para um servidor</span><span class="sxs-lookup"><span data-stu-id="78d65-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="78d65-112">Esse comando obtém o link de comunicação de servidor para servidor chamado Link01.</span><span class="sxs-lookup"><span data-stu-id="78d65-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="78d65-113">Exemplo 3: obter todos os links de comunicação para um servidor usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="78d65-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="78d65-114">Esse comando obtém todos os links de comunicação entre servidores para transações de banco de dados elástico para o servidor chamado ContosoServer17, que começa com "link".</span><span class="sxs-lookup"><span data-stu-id="78d65-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="78d65-115">OS</span><span class="sxs-lookup"><span data-stu-id="78d65-115">PARAMETERS</span></span>

### <span data-ttu-id="78d65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d65-116">-DefaultProfile</span></span>
<span data-ttu-id="78d65-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="78d65-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78d65-118">-LinkId</span><span class="sxs-lookup"><span data-stu-id="78d65-118">-LinkName</span></span>
<span data-ttu-id="78d65-119">Especifica o nome do link de comunicação do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="78d65-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="78d65-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d65-120">-ResourceGroupName</span></span>
<span data-ttu-id="78d65-121">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="78d65-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="78d65-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="78d65-122">-ServerName</span></span>
<span data-ttu-id="78d65-123">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="78d65-123">Specifies the name of a server.</span></span>
<span data-ttu-id="78d65-124">Este servidor contém um link de comunicação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="78d65-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78d65-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78d65-125">-Confirm</span></span>
<span data-ttu-id="78d65-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d65-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d65-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d65-127">-WhatIf</span></span>
<span data-ttu-id="78d65-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78d65-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d65-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78d65-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d65-130">CommonParameters</span></span>
<span data-ttu-id="78d65-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d65-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78d65-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d65-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78d65-133">INPUTS</span></span>

### <span data-ttu-id="78d65-134">System. String</span><span class="sxs-lookup"><span data-stu-id="78d65-134">System.String</span></span>

## <span data-ttu-id="78d65-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78d65-135">OUTPUTS</span></span>

### <span data-ttu-id="78d65-136">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="78d65-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="78d65-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78d65-137">NOTES</span></span>
* <span data-ttu-id="78d65-138">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="78d65-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="78d65-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78d65-139">RELATED LINKS</span></span>

[<span data-ttu-id="78d65-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="78d65-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="78d65-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="78d65-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="78d65-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="78d65-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
