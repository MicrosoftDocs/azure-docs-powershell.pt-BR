---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110909"
---
# <span data-ttu-id="e7828-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e7828-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="e7828-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7828-102">SYNOPSIS</span></span>
<span data-ttu-id="e7828-103">Exclui um link de comunicação para transações de banco de dados elásticas entre dois servidores.</span><span class="sxs-lookup"><span data-stu-id="e7828-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="e7828-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7828-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7828-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7828-105">DESCRIPTION</span></span>
<span data-ttu-id="e7828-106">O cmdlet **Remove-AzSqlServerCommunicationLink** exclui um link de comunicação de servidor para servidor para transações de banco de dados elásticas no Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7828-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="e7828-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e7828-107">EXAMPLES</span></span>

### <span data-ttu-id="e7828-108">Exemplo 1: Excluir um link de comunicação</span><span class="sxs-lookup"><span data-stu-id="e7828-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="e7828-109">Esse comando exclui um link de comunicação de servidor para servidor chamado Link01 no ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="e7828-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="e7828-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7828-110">PARAMETERS</span></span>

### <span data-ttu-id="e7828-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7828-111">-DefaultProfile</span></span>
<span data-ttu-id="e7828-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e7828-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7828-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e7828-113">-Force</span></span>
<span data-ttu-id="e7828-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e7828-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7828-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="e7828-115">-LinkName</span></span>
<span data-ttu-id="e7828-116">Especifica o nome do link de comunicação do servidor que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="e7828-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e7828-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7828-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7828-118">Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.</span><span class="sxs-lookup"><span data-stu-id="e7828-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="e7828-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7828-119">-ServerName</span></span>
<span data-ttu-id="e7828-120">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="e7828-120">Specifies the name of a server.</span></span>
<span data-ttu-id="e7828-121">Este servidor contém o link de comunicação que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="e7828-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e7828-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e7828-122">-Confirm</span></span>
<span data-ttu-id="e7828-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7828-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7828-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7828-124">-WhatIf</span></span>
<span data-ttu-id="e7828-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e7828-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7828-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7828-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7828-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7828-127">CommonParameters</span></span>
<span data-ttu-id="e7828-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7828-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7828-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7828-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7828-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="e7828-130">INPUTS</span></span>

### <span data-ttu-id="e7828-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e7828-131">System.String</span></span>

## <span data-ttu-id="e7828-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="e7828-132">OUTPUTS</span></span>

### <span data-ttu-id="e7828-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e7828-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="e7828-134">Notas</span><span class="sxs-lookup"><span data-stu-id="e7828-134">NOTES</span></span>
* <span data-ttu-id="e7828-135">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="e7828-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="e7828-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7828-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7828-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e7828-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e7828-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e7828-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e7828-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e7828-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
