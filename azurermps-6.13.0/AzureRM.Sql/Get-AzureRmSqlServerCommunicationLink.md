---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 3d53227f3d339419cfab5656de42fa52abb3bf08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431874"
---
# <span data-ttu-id="dc277-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dc277-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="dc277-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc277-102">SYNOPSIS</span></span>
<span data-ttu-id="dc277-103">Obtém links de comunicação para transações de banco de dados elástico entre servidores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dc277-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc277-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc277-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc277-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc277-105">DESCRIPTION</span></span>
<span data-ttu-id="dc277-106">O cmdlet **Get-AzureRmSqlServerCommunicationLink** Obtém links de comunicação entre servidores para transações de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc277-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="dc277-107">Especifique o nome de um link de comunicação do servidor para ver as propriedades desse link.</span><span class="sxs-lookup"><span data-stu-id="dc277-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="dc277-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc277-108">EXAMPLES</span></span>

### <span data-ttu-id="dc277-109">Exemplo 1: obter todos os links de comunicação para um servidor</span><span class="sxs-lookup"><span data-stu-id="dc277-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="dc277-110">Esse comando obtém todos os links de comunicação entre servidores para transações de banco de dados elástico para o servidor chamado ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="dc277-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="dc277-111">Exemplo 2: obter um link de comunicação específico para um servidor</span><span class="sxs-lookup"><span data-stu-id="dc277-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="dc277-112">Esse comando obtém o link de comunicação de servidor para servidor chamado Link01.</span><span class="sxs-lookup"><span data-stu-id="dc277-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="dc277-113">OS</span><span class="sxs-lookup"><span data-stu-id="dc277-113">PARAMETERS</span></span>

### <span data-ttu-id="dc277-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc277-114">-DefaultProfile</span></span>
<span data-ttu-id="dc277-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dc277-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc277-116">-LinkId</span><span class="sxs-lookup"><span data-stu-id="dc277-116">-LinkName</span></span>
<span data-ttu-id="dc277-117">Especifica o nome do link de comunicação do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="dc277-117">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dc277-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc277-118">-ResourceGroupName</span></span>
<span data-ttu-id="dc277-119">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="dc277-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="dc277-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="dc277-120">-ServerName</span></span>
<span data-ttu-id="dc277-121">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="dc277-121">Specifies the name of a server.</span></span>
<span data-ttu-id="dc277-122">Este servidor contém um link de comunicação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="dc277-122">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dc277-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc277-123">-Confirm</span></span>
<span data-ttu-id="dc277-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc277-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc277-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc277-125">-WhatIf</span></span>
<span data-ttu-id="dc277-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc277-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc277-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc277-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc277-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc277-128">CommonParameters</span></span>
<span data-ttu-id="dc277-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc277-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc277-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc277-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc277-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc277-131">INPUTS</span></span>

### <span data-ttu-id="dc277-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dc277-132">System.String</span></span>

## <span data-ttu-id="dc277-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc277-133">OUTPUTS</span></span>

### <span data-ttu-id="dc277-134">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="dc277-134">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="dc277-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc277-135">NOTES</span></span>
* <span data-ttu-id="dc277-136">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="dc277-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="dc277-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc277-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc277-138">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dc277-138">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="dc277-139">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dc277-139">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="dc277-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dc277-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
