---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 792d72c509df4c6b84f4ea86e597ddd8040a30d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440027"
---
# <span data-ttu-id="21c17-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="21c17-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="21c17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21c17-102">SYNOPSIS</span></span>
<span data-ttu-id="21c17-103">Obtém uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="21c17-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21c17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21c17-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21c17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21c17-105">DESCRIPTION</span></span>
<span data-ttu-id="21c17-106">O cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfiguration** Obtém uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="21c17-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="21c17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21c17-107">EXAMPLES</span></span>

## <span data-ttu-id="21c17-108">OS</span><span class="sxs-lookup"><span data-stu-id="21c17-108">PARAMETERS</span></span>

### <span data-ttu-id="21c17-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c17-109">-DefaultProfile</span></span>
<span data-ttu-id="21c17-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="21c17-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c17-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c17-111">-ResourceGroupName</span></span>
<span data-ttu-id="21c17-112">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21c17-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="21c17-113">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="21c17-113">-ServerName</span></span>
<span data-ttu-id="21c17-114">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="21c17-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="21c17-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="21c17-115">-VirtualEndpointName</span></span>
<span data-ttu-id="21c17-116">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="21c17-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c17-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21c17-117">-Confirm</span></span>
<span data-ttu-id="21c17-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21c17-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c17-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c17-119">-WhatIf</span></span>
<span data-ttu-id="21c17-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21c17-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c17-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21c17-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c17-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c17-122">CommonParameters</span></span>
<span data-ttu-id="21c17-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c17-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c17-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c17-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c17-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21c17-125">INPUTS</span></span>

### <span data-ttu-id="21c17-126">System. String</span><span class="sxs-lookup"><span data-stu-id="21c17-126">System.String</span></span>

## <span data-ttu-id="21c17-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21c17-127">OUTPUTS</span></span>

### <span data-ttu-id="21c17-128">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="21c17-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="21c17-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21c17-129">NOTES</span></span>

## <span data-ttu-id="21c17-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21c17-130">RELATED LINKS</span></span>

[<span data-ttu-id="21c17-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="21c17-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="21c17-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="21c17-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="21c17-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="21c17-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="21c17-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="21c17-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

