---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778419"
---
# <span data-ttu-id="dbdc6-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dbdc6-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="dbdc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbdc6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdc6-103">Cria um link de comunicação para transações de banco de dados elástico entre dois servidores de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="dbdc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbdc6-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbdc6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbdc6-105">DESCRIPTION</span></span>
<span data-ttu-id="dbdc6-106">O cmdlet **New-AzSqlServerCommunicationLink** cria um link de comunicação para transações de banco de dados elástico entre dois servidores lógicos no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="dbdc6-107">Transações de banco de dados elástico podem abranger bancos de dados em qualquer um dos servidores emparelhados.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="dbdc6-108">Você pode criar mais de um link em um servidor.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="dbdc6-109">Portanto, as transações de banco de dados elástico podem se estender por um número maior de servidores.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="dbdc6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbdc6-110">EXAMPLES</span></span>

### <span data-ttu-id="dbdc6-111">Exemplo 1: criar um link de comunicação</span><span class="sxs-lookup"><span data-stu-id="dbdc6-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="dbdc6-112">Esse comando cria um link chamado Link01 entre ContosoServer17 e ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="dbdc6-113">OS</span><span class="sxs-lookup"><span data-stu-id="dbdc6-113">PARAMETERS</span></span>

### <span data-ttu-id="dbdc6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbdc6-114">-AsJob</span></span>
<span data-ttu-id="dbdc6-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dbdc6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbdc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdc6-116">-DefaultProfile</span></span>
<span data-ttu-id="dbdc6-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dbdc6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbdc6-118">-LinkId</span><span class="sxs-lookup"><span data-stu-id="dbdc6-118">-LinkName</span></span>
<span data-ttu-id="dbdc6-119">Especifica o nome do link de comunicação do servidor que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdc6-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="dbdc6-120">-PartnerServer</span></span>
<span data-ttu-id="dbdc6-121">Especifica o nome do outro servidor que faz parte deste link de comunicação.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdc6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdc6-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbdc6-123">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="dbdc6-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="dbdc6-124">-ServerName</span></span>
<span data-ttu-id="dbdc6-125">Especifica o nome do servidor no qual esse cmdlet configura o link de comunicação.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="dbdc6-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dbdc6-126">-Confirm</span></span>
<span data-ttu-id="dbdc6-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbdc6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdc6-128">-WhatIf</span></span>
<span data-ttu-id="dbdc6-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbdc6-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbdc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdc6-131">CommonParameters</span></span>
<span data-ttu-id="dbdc6-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdc6-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbdc6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdc6-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbdc6-134">INPUTS</span></span>

### <span data-ttu-id="dbdc6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dbdc6-135">System.String</span></span>

## <span data-ttu-id="dbdc6-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbdc6-136">OUTPUTS</span></span>

### <span data-ttu-id="dbdc6-137">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="dbdc6-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="dbdc6-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbdc6-138">NOTES</span></span>
* <span data-ttu-id="dbdc6-139">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="dbdc6-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="dbdc6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbdc6-140">RELATED LINKS</span></span>

[<span data-ttu-id="dbdc6-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dbdc6-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="dbdc6-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dbdc6-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="dbdc6-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dbdc6-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
