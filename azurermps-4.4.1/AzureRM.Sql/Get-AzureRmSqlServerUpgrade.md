---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d2a92e7209745873364b5de114916bc48b0a3b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427766"
---
# <span data-ttu-id="a5fea-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="a5fea-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="a5fea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5fea-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fea-103">Obtém o status de uma atualização do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5fea-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5fea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5fea-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5fea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5fea-105">DESCRIPTION</span></span>
<span data-ttu-id="a5fea-106">O cmdlet **Get-AzureRmSqlServerUpgrade** Obtém o status de uma atualização do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5fea-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="a5fea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5fea-107">EXAMPLES</span></span>

### <span data-ttu-id="a5fea-108">Exemplo 1: obter o status de uma atualização</span><span class="sxs-lookup"><span data-stu-id="a5fea-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="a5fea-109">Esse comando obtém o status de uma atualização do servidor chamado Server01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a5fea-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a5fea-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5fea-110">PARAMETERS</span></span>

### <span data-ttu-id="a5fea-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5fea-111">-ResourceGroupName</span></span>
<span data-ttu-id="a5fea-112">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a5fea-112">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a5fea-113">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a5fea-113">-ServerName</span></span>
<span data-ttu-id="a5fea-114">Especifica o nome do servidor para o qual esse cmdlet obtém o status de atualização.</span><span class="sxs-lookup"><span data-stu-id="a5fea-114">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fea-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5fea-115">-Confirm</span></span>
<span data-ttu-id="a5fea-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5fea-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5fea-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5fea-117">-WhatIf</span></span>
<span data-ttu-id="a5fea-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5fea-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5fea-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5fea-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5fea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fea-120">-DefaultProfile</span></span>
<span data-ttu-id="a5fea-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5fea-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5fea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fea-122">CommonParameters</span></span>
<span data-ttu-id="a5fea-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5fea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fea-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5fea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fea-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5fea-125">INPUTS</span></span>

## <span data-ttu-id="a5fea-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5fea-126">OUTPUTS</span></span>

### <span data-ttu-id="a5fea-127">Microsoft. Azure. Commands. Sql. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="a5fea-127">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="a5fea-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5fea-128">NOTES</span></span>

## <span data-ttu-id="a5fea-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5fea-129">RELATED LINKS</span></span>

[<span data-ttu-id="a5fea-130">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="a5fea-130">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="a5fea-131">Parar-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="a5fea-131">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="a5fea-132">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="a5fea-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


