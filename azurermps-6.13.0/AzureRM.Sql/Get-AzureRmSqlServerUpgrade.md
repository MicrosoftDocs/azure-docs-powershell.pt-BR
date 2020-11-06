---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 7f48385c7002f353ca34f399d40310a9e0469977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427145"
---
# <span data-ttu-id="393cf-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="393cf-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="393cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="393cf-102">SYNOPSIS</span></span>
<span data-ttu-id="393cf-103">Obtém o status de uma atualização do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="393cf-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="393cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="393cf-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="393cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="393cf-105">DESCRIPTION</span></span>
<span data-ttu-id="393cf-106">O cmdlet **Get-AzureRmSqlServerUpgrade** Obtém o status de uma atualização do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="393cf-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="393cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="393cf-107">EXAMPLES</span></span>

### <span data-ttu-id="393cf-108">Exemplo 1: obter o status de uma atualização</span><span class="sxs-lookup"><span data-stu-id="393cf-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="393cf-109">Esse comando obtém o status de uma atualização do servidor chamado Server01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="393cf-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="393cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="393cf-110">PARAMETERS</span></span>

### <span data-ttu-id="393cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393cf-111">-DefaultProfile</span></span>
<span data-ttu-id="393cf-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="393cf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="393cf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393cf-113">-ResourceGroupName</span></span>
<span data-ttu-id="393cf-114">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="393cf-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="393cf-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="393cf-115">-ServerName</span></span>
<span data-ttu-id="393cf-116">Especifica o nome do servidor para o qual esse cmdlet obtém o status de atualização.</span><span class="sxs-lookup"><span data-stu-id="393cf-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="393cf-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="393cf-117">-Confirm</span></span>
<span data-ttu-id="393cf-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="393cf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="393cf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="393cf-119">-WhatIf</span></span>
<span data-ttu-id="393cf-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="393cf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="393cf-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="393cf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="393cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393cf-122">CommonParameters</span></span>
<span data-ttu-id="393cf-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393cf-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393cf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393cf-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="393cf-125">INPUTS</span></span>

### <span data-ttu-id="393cf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="393cf-126">System.String</span></span>

## <span data-ttu-id="393cf-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="393cf-127">OUTPUTS</span></span>

### <span data-ttu-id="393cf-128">Microsoft. Azure. Commands. Sql. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="393cf-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="393cf-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="393cf-129">NOTES</span></span>

## <span data-ttu-id="393cf-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="393cf-130">RELATED LINKS</span></span>

[<span data-ttu-id="393cf-131">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="393cf-131">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="393cf-132">Parar-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="393cf-132">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="393cf-133">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="393cf-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


