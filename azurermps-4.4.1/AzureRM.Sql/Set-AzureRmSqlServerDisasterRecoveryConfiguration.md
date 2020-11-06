---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610981"
---
# <span data-ttu-id="ca5d0-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d0-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ca5d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5d0-103">Modifica uma configuração de recuperação do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca5d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca5d0-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca5d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca5d0-105">DESCRIPTION</span></span>
<span data-ttu-id="ca5d0-106">O cmdlet **set-AzureRmSqlServerDisasterRecoveryConfiguration** modifica uma configuração de recuperação do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="ca5d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca5d0-107">EXAMPLES</span></span>

## <span data-ttu-id="ca5d0-108">OS</span><span class="sxs-lookup"><span data-stu-id="ca5d0-108">PARAMETERS</span></span>

### <span data-ttu-id="ca5d0-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ca5d0-109">-AllowDataLoss</span></span>
<span data-ttu-id="ca5d0-110">Indica que a operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="ca5d0-111">-Failover</span><span class="sxs-lookup"><span data-stu-id="ca5d0-111">-Failover</span></span>
<span data-ttu-id="ca5d0-112">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-112">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5d0-113">-ResourceGroupName</span></span>
<span data-ttu-id="ca5d0-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ca5d0-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ca5d0-115">-ServerName</span></span>
<span data-ttu-id="ca5d0-116">Especifica o nome de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="ca5d0-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ca5d0-117">-VirtualEndpointName</span></span>
<span data-ttu-id="ca5d0-118">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5d0-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca5d0-119">-Confirm</span></span>
<span data-ttu-id="ca5d0-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca5d0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5d0-121">-WhatIf</span></span>
<span data-ttu-id="ca5d0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca5d0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca5d0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5d0-124">-DefaultProfile</span></span>
<span data-ttu-id="ca5d0-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca5d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5d0-126">CommonParameters</span></span>
<span data-ttu-id="ca5d0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5d0-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca5d0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5d0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca5d0-129">INPUTS</span></span>

## <span data-ttu-id="ca5d0-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca5d0-130">OUTPUTS</span></span>

## <span data-ttu-id="ca5d0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca5d0-131">NOTES</span></span>

## <span data-ttu-id="ca5d0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca5d0-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca5d0-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d0-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ca5d0-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d0-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ca5d0-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca5d0-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ca5d0-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ca5d0-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
