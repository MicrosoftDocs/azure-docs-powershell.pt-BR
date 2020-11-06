---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: d78b2fafb6c633c8a0276193e9e42677de814ff3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602397"
---
# <span data-ttu-id="f715b-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f715b-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="f715b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f715b-102">SYNOPSIS</span></span>
<span data-ttu-id="f715b-103">Obtém o status das operações em um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f715b-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f715b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f715b-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f715b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f715b-105">DESCRIPTION</span></span>
<span data-ttu-id="f715b-106">O cmdlet **Get-AzureRmSqlElasticPoolActivity** Obtém o status das operações em um pool elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f715b-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="f715b-107">Você pode ver o status da criação e das atualizações de configuração do pool.</span><span class="sxs-lookup"><span data-stu-id="f715b-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="f715b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f715b-108">EXAMPLES</span></span>

### <span data-ttu-id="f715b-109">Exemplo 1: obter o status das operações para um pool elástico</span><span class="sxs-lookup"><span data-stu-id="f715b-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f715b-110">Esse comando obtém o status das operações do pool elástico chamado ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="f715b-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="f715b-111">OS</span><span class="sxs-lookup"><span data-stu-id="f715b-111">PARAMETERS</span></span>

### <span data-ttu-id="f715b-112">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f715b-112">-ElasticPoolName</span></span>
<span data-ttu-id="f715b-113">Especifica o nome de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f715b-113">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="f715b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f715b-114">-ResourceGroupName</span></span>
<span data-ttu-id="f715b-115">Especifica o nome de um grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f715b-115">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f715b-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f715b-116">-ServerName</span></span>
<span data-ttu-id="f715b-117">Especifica o nome de um servidor que contém um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f715b-117">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="f715b-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f715b-118">-Confirm</span></span>
<span data-ttu-id="f715b-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f715b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f715b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f715b-120">-WhatIf</span></span>
<span data-ttu-id="f715b-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f715b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f715b-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f715b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f715b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f715b-123">-DefaultProfile</span></span>
<span data-ttu-id="f715b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f715b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f715b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f715b-125">CommonParameters</span></span>
<span data-ttu-id="f715b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f715b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f715b-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f715b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f715b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f715b-128">INPUTS</span></span>

## <span data-ttu-id="f715b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f715b-129">OUTPUTS</span></span>

### <span data-ttu-id="f715b-130">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="f715b-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="f715b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f715b-131">NOTES</span></span>

## <span data-ttu-id="f715b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f715b-132">RELATED LINKS</span></span>

[<span data-ttu-id="f715b-133">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f715b-133">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f715b-134">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f715b-134">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="f715b-135">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f715b-135">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f715b-136">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f715b-136">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f715b-137">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f715b-137">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


