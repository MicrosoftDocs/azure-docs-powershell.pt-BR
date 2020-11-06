---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1b8e99b195866ac63f649d4484a0cfb631b09e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426542"
---
# <span data-ttu-id="57158-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="57158-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="57158-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57158-102">SYNOPSIS</span></span>
<span data-ttu-id="57158-103">Interrompe a atualização de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="57158-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57158-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57158-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57158-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57158-105">DESCRIPTION</span></span>
<span data-ttu-id="57158-106">O cmdlet **Stop-AzureRmSqlServerUpgrade** interrompe a atualização de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="57158-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="57158-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57158-107">EXAMPLES</span></span>

### <span data-ttu-id="57158-108">Exemplo 1: parar uma atualização do servidor</span><span class="sxs-lookup"><span data-stu-id="57158-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="57158-109">Esse comando interrompe a solicitação de atualização do servidor chamado Server02 atribuído ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="57158-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="57158-110">OS</span><span class="sxs-lookup"><span data-stu-id="57158-110">PARAMETERS</span></span>

### <span data-ttu-id="57158-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57158-111">-DefaultProfile</span></span>
<span data-ttu-id="57158-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="57158-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57158-113">-Force</span><span class="sxs-lookup"><span data-stu-id="57158-113">-Force</span></span>
<span data-ttu-id="57158-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="57158-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57158-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57158-115">-ResourceGroupName</span></span>
<span data-ttu-id="57158-116">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="57158-116">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57158-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="57158-117">-ServerName</span></span>
<span data-ttu-id="57158-118">Especifica o nome do servidor para o qual esse cmdlet interrompe uma atualização.</span><span class="sxs-lookup"><span data-stu-id="57158-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57158-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57158-119">-Confirm</span></span>
<span data-ttu-id="57158-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57158-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57158-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57158-121">-WhatIf</span></span>
<span data-ttu-id="57158-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57158-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57158-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57158-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57158-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57158-124">CommonParameters</span></span>
<span data-ttu-id="57158-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57158-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57158-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57158-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57158-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57158-127">INPUTS</span></span>

### <span data-ttu-id="57158-128">Microsoft. Azure. Commands. Sql. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="57158-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="57158-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57158-129">OUTPUTS</span></span>

## <span data-ttu-id="57158-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57158-130">NOTES</span></span>

## <span data-ttu-id="57158-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57158-131">RELATED LINKS</span></span>

[<span data-ttu-id="57158-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="57158-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="57158-133">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="57158-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="57158-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="57158-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


