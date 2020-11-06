---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ed968db32505bcb3c581775d05235cc4c718dd67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432168"
---
# <span data-ttu-id="19aa2-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="19aa2-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="19aa2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="19aa2-103">Obtém links de comunicação para transações de banco de dados elástico entre servidores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="19aa2-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19aa2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19aa2-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19aa2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19aa2-105">DESCRIPTION</span></span>
<span data-ttu-id="19aa2-106">O cmdlet **Get-AzureRmSqlServerCommunicationLink** Obtém links de comunicação entre servidores para transações de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="19aa2-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="19aa2-107">Especifique o nome de um link de comunicação do servidor para ver as propriedades desse link.</span><span class="sxs-lookup"><span data-stu-id="19aa2-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="19aa2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19aa2-108">EXAMPLES</span></span>

### <span data-ttu-id="19aa2-109">Exemplo 1: obter todos os links de comunicação para um servidor</span><span class="sxs-lookup"><span data-stu-id="19aa2-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="19aa2-110">Esse comando obtém todos os links de comunicação entre servidores para transações de banco de dados elástico para o servidor chamado ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="19aa2-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="19aa2-111">Exemplo 2: obter um link de comunicação específico para um servidor</span><span class="sxs-lookup"><span data-stu-id="19aa2-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="19aa2-112">Esse comando obtém o link de comunicação de servidor para servidor chamado Link01.</span><span class="sxs-lookup"><span data-stu-id="19aa2-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="19aa2-113">OS</span><span class="sxs-lookup"><span data-stu-id="19aa2-113">PARAMETERS</span></span>

### <span data-ttu-id="19aa2-114">-LinkId</span><span class="sxs-lookup"><span data-stu-id="19aa2-114">-LinkName</span></span>
<span data-ttu-id="19aa2-115">Especifica o nome do link de comunicação do servidor que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19aa2-115">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19aa2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19aa2-116">-ResourceGroupName</span></span>
<span data-ttu-id="19aa2-117">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="19aa2-117">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="19aa2-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="19aa2-118">-ServerName</span></span>
<span data-ttu-id="19aa2-119">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="19aa2-119">Specifies the name of a server.</span></span>
<span data-ttu-id="19aa2-120">Este servidor contém um link de comunicação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19aa2-120">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19aa2-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19aa2-121">-Confirm</span></span>
<span data-ttu-id="19aa2-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19aa2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19aa2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19aa2-123">-WhatIf</span></span>
<span data-ttu-id="19aa2-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19aa2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19aa2-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19aa2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19aa2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19aa2-126">-DefaultProfile</span></span>
<span data-ttu-id="19aa2-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19aa2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19aa2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19aa2-128">CommonParameters</span></span>
<span data-ttu-id="19aa2-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19aa2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19aa2-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19aa2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19aa2-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19aa2-131">INPUTS</span></span>

## <span data-ttu-id="19aa2-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19aa2-132">OUTPUTS</span></span>

### <span data-ttu-id="19aa2-133">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="19aa2-133">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="19aa2-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19aa2-134">NOTES</span></span>
* <span data-ttu-id="19aa2-135">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="19aa2-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="19aa2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19aa2-136">RELATED LINKS</span></span>

[<span data-ttu-id="19aa2-137">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="19aa2-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="19aa2-138">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="19aa2-138">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="19aa2-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="19aa2-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
