---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 3d2137aa1398e5bb3b8173b6ea927c4deb50d41f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610535"
---
# <span data-ttu-id="bb16d-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bb16d-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="bb16d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb16d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb16d-103">Exclui um link de comunicação para transações de banco de dados elástico entre dois servidores.</span><span class="sxs-lookup"><span data-stu-id="bb16d-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb16d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb16d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb16d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb16d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb16d-106">O cmdlet **Remove-AzureRmSqlServerCommunicationLink** exclui um link de comunicação de servidor para servidor para transações de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb16d-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="bb16d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb16d-107">EXAMPLES</span></span>

### <span data-ttu-id="bb16d-108">Exemplo 1: excluir um link de comunicação</span><span class="sxs-lookup"><span data-stu-id="bb16d-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="bb16d-109">Esse comando exclui um link de comunicação de servidor para servidor chamado Link01 em ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="bb16d-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="bb16d-110">OS</span><span class="sxs-lookup"><span data-stu-id="bb16d-110">PARAMETERS</span></span>

### <span data-ttu-id="bb16d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb16d-111">-DefaultProfile</span></span>
<span data-ttu-id="bb16d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb16d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb16d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bb16d-113">-Force</span></span>
<span data-ttu-id="bb16d-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bb16d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb16d-115">-LinkId</span><span class="sxs-lookup"><span data-stu-id="bb16d-115">-LinkName</span></span>
<span data-ttu-id="bb16d-116">Especifica o nome do link de comunicação do servidor que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="bb16d-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bb16d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb16d-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb16d-118">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="bb16d-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="bb16d-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bb16d-119">-ServerName</span></span>
<span data-ttu-id="bb16d-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="bb16d-120">Specifies the name of a server.</span></span>
<span data-ttu-id="bb16d-121">Esse servidor contém o link de comunicação que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="bb16d-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="bb16d-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb16d-122">-Confirm</span></span>
<span data-ttu-id="bb16d-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb16d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb16d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb16d-124">-WhatIf</span></span>
<span data-ttu-id="bb16d-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb16d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb16d-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb16d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb16d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb16d-127">CommonParameters</span></span>
<span data-ttu-id="bb16d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb16d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb16d-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb16d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb16d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb16d-130">INPUTS</span></span>

### <span data-ttu-id="bb16d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bb16d-131">System.String</span></span>

## <span data-ttu-id="bb16d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb16d-132">OUTPUTS</span></span>

### <span data-ttu-id="bb16d-133">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="bb16d-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="bb16d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb16d-134">NOTES</span></span>
* <span data-ttu-id="bb16d-135">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="bb16d-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="bb16d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb16d-136">RELATED LINKS</span></span>

[<span data-ttu-id="bb16d-137">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bb16d-137">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="bb16d-138">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="bb16d-138">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="bb16d-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="bb16d-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
