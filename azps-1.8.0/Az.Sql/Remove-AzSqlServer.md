---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 52e0d37777b349744cf82f891fe8f711758f5a64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598839"
---
# <span data-ttu-id="05d74-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05d74-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="05d74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05d74-102">SYNOPSIS</span></span>
<span data-ttu-id="05d74-103">Remove um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="05d74-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="05d74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05d74-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05d74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05d74-105">DESCRIPTION</span></span>
<span data-ttu-id="05d74-106">O cmdlet **Remove-AzSqlServer** remove um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="05d74-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="05d74-107">A operação de exclusão é assíncrona e pode demorar algum tempo, portanto verifique se a operação foi concluída antes de executar qualquer operação adicional que dependa do servidor ser completamente excluído.</span><span class="sxs-lookup"><span data-stu-id="05d74-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="05d74-108">Por exemplo, você precisa criar um novo servidor que use o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="05d74-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="05d74-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05d74-109">EXAMPLES</span></span>

### <span data-ttu-id="05d74-110">Exemplo 1: remover um servidor</span><span class="sxs-lookup"><span data-stu-id="05d74-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="05d74-111">Esse comando Remove o servidor do banco de dados SQL do Azure chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="05d74-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="05d74-112">OS</span><span class="sxs-lookup"><span data-stu-id="05d74-112">PARAMETERS</span></span>

### <span data-ttu-id="05d74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d74-113">-DefaultProfile</span></span>
<span data-ttu-id="05d74-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="05d74-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05d74-115">-Force</span><span class="sxs-lookup"><span data-stu-id="05d74-115">-Force</span></span>
<span data-ttu-id="05d74-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="05d74-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05d74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d74-117">-ResourceGroupName</span></span>
<span data-ttu-id="05d74-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="05d74-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="05d74-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="05d74-119">-ServerName</span></span>
<span data-ttu-id="05d74-120">Especifica o nome do servidor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="05d74-120">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="05d74-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05d74-121">-Confirm</span></span>
<span data-ttu-id="05d74-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05d74-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05d74-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05d74-123">-WhatIf</span></span>
<span data-ttu-id="05d74-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05d74-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05d74-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05d74-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05d74-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d74-126">CommonParameters</span></span>
<span data-ttu-id="05d74-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d74-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d74-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05d74-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d74-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05d74-129">INPUTS</span></span>

### <span data-ttu-id="05d74-130">System. String</span><span class="sxs-lookup"><span data-stu-id="05d74-130">System.String</span></span>

## <span data-ttu-id="05d74-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05d74-131">OUTPUTS</span></span>

### <span data-ttu-id="05d74-132">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="05d74-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="05d74-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05d74-133">NOTES</span></span>

## <span data-ttu-id="05d74-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05d74-134">RELATED LINKS</span></span>

[<span data-ttu-id="05d74-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05d74-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="05d74-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05d74-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="05d74-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05d74-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="05d74-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="05d74-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


