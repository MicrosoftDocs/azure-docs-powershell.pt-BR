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
ms.locfileid: "93773879"
---
# <span data-ttu-id="90021-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="90021-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="90021-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90021-102">SYNOPSIS</span></span>
<span data-ttu-id="90021-103">Obtém links de comunicação para transações de banco de dados elástico entre servidores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="90021-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="90021-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90021-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90021-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90021-105">DESCRIPTION</span></span>
<span data-ttu-id="90021-106">O cmdlet **Get-AzSqlServerCommunicationLink** Obtém links de comunicação entre servidores para transações de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="90021-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="90021-107">Especifique o nome de um link de comunicação do servidor para ver as propriedades desse link.</span><span class="sxs-lookup"><span data-stu-id="90021-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="90021-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90021-108">EXAMPLES</span></span>

### <span data-ttu-id="90021-109">Exemplo 1: obter todos os links de comunicação para um servidor</span><span class="sxs-lookup"><span data-stu-id="90021-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="90021-110">Esse comando obtém todos os links de comunicação entre servidores para transações de banco de dados elástico para o servidor chamado ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="90021-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="90021-111">Exemplo 2: obter um link de comunicação específico para um servidor</span><span class="sxs-lookup"><span data-stu-id="90021-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="90021-112">Esse comando obtém o link de comunicação de servidor para servidor chamado Link01.</span><span class="sxs-lookup"><span data-stu-id="90021-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="90021-113">Exemplo 3: obter todos os links de comunicação para um servidor usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="90021-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="90021-114">Esse comando obtém todos os links de comunicação entre servidores para transações de banco de dados elástico para o servidor chamado ContosoServer17, que começa com "link".</span><span class="sxs-lookup"><span data-stu-id="90021-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="90021-115">OS</span><span class="sxs-lookup"><span data-stu-id="90021-115">PARAMETERS</span></span>

### <span data-ttu-id="90021-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90021-116">-DefaultProfile</span></span>
<span data-ttu-id="90021-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="90021-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90021-118">-LinkId</span><span class="sxs-lookup"><span data-stu-id="90021-118">-LinkName</span></span>
<span data-ttu-id="90021-119">Especifica o nome do link de comunicação do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="90021-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="90021-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90021-120">-ResourceGroupName</span></span>
<span data-ttu-id="90021-121">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="90021-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="90021-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="90021-122">-ServerName</span></span>
<span data-ttu-id="90021-123">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="90021-123">Specifies the name of a server.</span></span>
<span data-ttu-id="90021-124">Este servidor contém um link de comunicação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="90021-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="90021-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="90021-125">-Confirm</span></span>
<span data-ttu-id="90021-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90021-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90021-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90021-127">-WhatIf</span></span>
<span data-ttu-id="90021-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90021-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90021-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90021-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90021-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90021-130">CommonParameters</span></span>
<span data-ttu-id="90021-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90021-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90021-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90021-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90021-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90021-133">INPUTS</span></span>

### <span data-ttu-id="90021-134">System. String</span><span class="sxs-lookup"><span data-stu-id="90021-134">System.String</span></span>

## <span data-ttu-id="90021-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90021-135">OUTPUTS</span></span>

### <span data-ttu-id="90021-136">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="90021-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="90021-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90021-137">NOTES</span></span>
* <span data-ttu-id="90021-138">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="90021-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="90021-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90021-139">RELATED LINKS</span></span>

[<span data-ttu-id="90021-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="90021-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="90021-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="90021-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="90021-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="90021-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
