---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264688"
---
# <span data-ttu-id="d9914-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d9914-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="d9914-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9914-102">SYNOPSIS</span></span>
<span data-ttu-id="d9914-103">Exclui um link de comunicação para transações de banco de dados elástico entre dois servidores.</span><span class="sxs-lookup"><span data-stu-id="d9914-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="d9914-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9914-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9914-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9914-105">DESCRIPTION</span></span>
<span data-ttu-id="d9914-106">O cmdlet **Remove-AzSqlServerCommunicationLink** exclui um link de comunicação de servidor para servidor para transações de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9914-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="d9914-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9914-107">EXAMPLES</span></span>

### <span data-ttu-id="d9914-108">Exemplo 1: excluir um link de comunicação</span><span class="sxs-lookup"><span data-stu-id="d9914-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="d9914-109">Esse comando exclui um link de comunicação de servidor para servidor chamado Link01 em ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="d9914-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="d9914-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9914-110">PARAMETERS</span></span>

### <span data-ttu-id="d9914-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9914-111">-DefaultProfile</span></span>
<span data-ttu-id="d9914-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d9914-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9914-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d9914-113">-Force</span></span>
<span data-ttu-id="d9914-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d9914-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9914-115">-LinkId</span><span class="sxs-lookup"><span data-stu-id="d9914-115">-LinkName</span></span>
<span data-ttu-id="d9914-116">Especifica o nome do link de comunicação do servidor que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="d9914-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="d9914-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9914-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9914-118">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="d9914-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="d9914-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d9914-119">-ServerName</span></span>
<span data-ttu-id="d9914-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="d9914-120">Specifies the name of a server.</span></span>
<span data-ttu-id="d9914-121">Esse servidor contém o link de comunicação que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="d9914-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="d9914-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9914-122">-Confirm</span></span>
<span data-ttu-id="d9914-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9914-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9914-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9914-124">-WhatIf</span></span>
<span data-ttu-id="d9914-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9914-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9914-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9914-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9914-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9914-127">CommonParameters</span></span>
<span data-ttu-id="d9914-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9914-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9914-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9914-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9914-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9914-130">INPUTS</span></span>

### <span data-ttu-id="d9914-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d9914-131">System.String</span></span>

## <span data-ttu-id="d9914-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9914-132">OUTPUTS</span></span>

### <span data-ttu-id="d9914-133">Microsoft. Azure. Commands. Sql. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d9914-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="d9914-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9914-134">NOTES</span></span>
* <span data-ttu-id="d9914-135">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d9914-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d9914-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9914-136">RELATED LINKS</span></span>

[<span data-ttu-id="d9914-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d9914-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d9914-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d9914-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d9914-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d9914-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
