---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 48b1ee50f1ebd0003097500849a6d03dac64c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441373"
---
# <span data-ttu-id="f8c93-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="f8c93-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="f8c93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8c93-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c93-103">Remove um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c93-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8c93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8c93-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8c93-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8c93-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c93-106">O cmdlet **Remove-AzureRmSqlServer** remove um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c93-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="f8c93-107">A operação de exclusão é assíncrona e pode demorar algum tempo, portanto verifique se a operação foi concluída antes de executar qualquer operação adicional que dependa do servidor ser completamente excluído.</span><span class="sxs-lookup"><span data-stu-id="f8c93-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="f8c93-108">Por exemplo, você precisa criar um novo servidor que use o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="f8c93-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="f8c93-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8c93-109">EXAMPLES</span></span>

### <span data-ttu-id="f8c93-110">Exemplo 1: remover um servidor</span><span class="sxs-lookup"><span data-stu-id="f8c93-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="f8c93-111">Esse comando Remove o servidor do banco de dados SQL do Azure chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="f8c93-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="f8c93-112">OS</span><span class="sxs-lookup"><span data-stu-id="f8c93-112">PARAMETERS</span></span>

### <span data-ttu-id="f8c93-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f8c93-113">-Force</span></span>
<span data-ttu-id="f8c93-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f8c93-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8c93-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c93-115">-ResourceGroupName</span></span>
<span data-ttu-id="f8c93-116">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f8c93-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f8c93-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f8c93-117">-ServerName</span></span>
<span data-ttu-id="f8c93-118">Especifica o nome do servidor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f8c93-118">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="f8c93-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f8c93-119">-Confirm</span></span>
<span data-ttu-id="f8c93-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8c93-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c93-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c93-121">-WhatIf</span></span>
<span data-ttu-id="f8c93-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f8c93-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8c93-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f8c93-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c93-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c93-124">-DefaultProfile</span></span>
<span data-ttu-id="f8c93-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c93-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c93-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c93-126">CommonParameters</span></span>
<span data-ttu-id="f8c93-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c93-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c93-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8c93-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c93-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8c93-129">INPUTS</span></span>

### <span data-ttu-id="f8c93-130">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f8c93-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="f8c93-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8c93-131">OUTPUTS</span></span>

### <span data-ttu-id="f8c93-132">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f8c93-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="f8c93-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8c93-133">NOTES</span></span>

## <span data-ttu-id="f8c93-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8c93-134">RELATED LINKS</span></span>

[<span data-ttu-id="f8c93-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="f8c93-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="f8c93-136">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="f8c93-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="f8c93-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="f8c93-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="f8c93-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f8c93-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


