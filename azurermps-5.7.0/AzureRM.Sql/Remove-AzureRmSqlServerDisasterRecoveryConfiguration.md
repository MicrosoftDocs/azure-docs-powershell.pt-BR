---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 7b5c793bda8b05b78ce97e1f164126de62102fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429656"
---
# <span data-ttu-id="0afbd-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afbd-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="0afbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0afbd-102">SYNOPSIS</span></span>
<span data-ttu-id="0afbd-103">Remove uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0afbd-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0afbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0afbd-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0afbd-105">DESCRIPTION</span></span>
<span data-ttu-id="0afbd-106">O cmdlet **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** remove uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0afbd-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="0afbd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0afbd-107">EXAMPLES</span></span>

## <span data-ttu-id="0afbd-108">OS</span><span class="sxs-lookup"><span data-stu-id="0afbd-108">PARAMETERS</span></span>

### <span data-ttu-id="0afbd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afbd-109">-DefaultProfile</span></span>
<span data-ttu-id="0afbd-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0afbd-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0afbd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0afbd-111">-Force</span></span>
<span data-ttu-id="0afbd-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0afbd-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0afbd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afbd-113">-ResourceGroupName</span></span>
<span data-ttu-id="0afbd-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0afbd-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0afbd-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0afbd-115">-ServerName</span></span>
<span data-ttu-id="0afbd-116">Especifica o nome de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0afbd-116">Specifies the name of a SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0afbd-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="0afbd-117">-VirtualEndpointName</span></span>
<span data-ttu-id="0afbd-118">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="0afbd-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0afbd-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0afbd-119">-Confirm</span></span>
<span data-ttu-id="0afbd-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afbd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afbd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afbd-121">-WhatIf</span></span>
<span data-ttu-id="0afbd-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0afbd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afbd-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0afbd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afbd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afbd-124">CommonParameters</span></span>
<span data-ttu-id="0afbd-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afbd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afbd-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afbd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afbd-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0afbd-127">INPUTS</span></span>

### <span data-ttu-id="0afbd-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0afbd-128">None</span></span>
<span data-ttu-id="0afbd-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0afbd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0afbd-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0afbd-130">OUTPUTS</span></span>

## <span data-ttu-id="0afbd-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0afbd-131">NOTES</span></span>

## <span data-ttu-id="0afbd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0afbd-132">RELATED LINKS</span></span>

[<span data-ttu-id="0afbd-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afbd-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0afbd-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afbd-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0afbd-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afbd-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0afbd-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0afbd-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
