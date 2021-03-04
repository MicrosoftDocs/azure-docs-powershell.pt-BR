---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: b116a6ef09b3de4d3a11c1e9bdbcb831fc34af1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887308"
---
# <span data-ttu-id="51cae-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="51cae-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="51cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51cae-102">SYNOPSIS</span></span>
<span data-ttu-id="51cae-103">Remove um servidor de banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="51cae-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="51cae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51cae-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51cae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51cae-105">DESCRIPTION</span></span>
<span data-ttu-id="51cae-106">O cmdlet **Remove-AzSqlServer** remove um servidor de banco de dados do Azure SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="51cae-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="51cae-107">A operação de exclusão é assíncrona e pode levar algum tempo, portanto, verifique se a operação foi concluída antes de executar quaisquer operações adicionais que dependam do servidor ser completamente excluído.</span><span class="sxs-lookup"><span data-stu-id="51cae-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="51cae-108">Por exemplo, você precisa criar um novo servidor que use o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="51cae-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="51cae-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51cae-109">EXAMPLES</span></span>

### <span data-ttu-id="51cae-110">Exemplo 1: Remover um servidor</span><span class="sxs-lookup"><span data-stu-id="51cae-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="51cae-111">Este comando remove o servidor de banco de dados do Azure SQL chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="51cae-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="51cae-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51cae-112">PARAMETERS</span></span>

### <span data-ttu-id="51cae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51cae-113">-DefaultProfile</span></span>
<span data-ttu-id="51cae-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="51cae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51cae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="51cae-115">-Force</span></span>
<span data-ttu-id="51cae-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="51cae-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51cae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51cae-117">-ResourceGroupName</span></span>
<span data-ttu-id="51cae-118">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="51cae-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="51cae-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="51cae-119">-ServerName</span></span>
<span data-ttu-id="51cae-120">Especifica o nome do servidor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="51cae-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51cae-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51cae-121">-Confirm</span></span>
<span data-ttu-id="51cae-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51cae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51cae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51cae-123">-WhatIf</span></span>
<span data-ttu-id="51cae-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51cae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51cae-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51cae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51cae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cae-126">CommonParameters</span></span>
<span data-ttu-id="51cae-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51cae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cae-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51cae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cae-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51cae-129">INPUTS</span></span>

### <span data-ttu-id="51cae-130">System.String</span><span class="sxs-lookup"><span data-stu-id="51cae-130">System.String</span></span>

## <span data-ttu-id="51cae-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51cae-131">OUTPUTS</span></span>

### <span data-ttu-id="51cae-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="51cae-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="51cae-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="51cae-133">NOTES</span></span>

## <span data-ttu-id="51cae-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51cae-134">RELATED LINKS</span></span>

[<span data-ttu-id="51cae-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="51cae-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="51cae-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="51cae-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="51cae-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="51cae-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="51cae-138">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="51cae-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


