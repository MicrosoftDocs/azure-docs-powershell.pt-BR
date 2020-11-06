---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 3c67c432f8f49927af4cbf357a4338f528c826b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433369"
---
# <span data-ttu-id="cb039-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="cb039-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="cb039-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb039-102">SYNOPSIS</span></span>
<span data-ttu-id="cb039-103">Obtém a atividade para uma configuração de recuperação do sistema do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cb039-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb039-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb039-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb039-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb039-105">DESCRIPTION</span></span>
<span data-ttu-id="cb039-106">O cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** Obtém atividade para uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="cb039-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="cb039-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb039-107">EXAMPLES</span></span>

## <span data-ttu-id="cb039-108">OS</span><span class="sxs-lookup"><span data-stu-id="cb039-108">PARAMETERS</span></span>

### <span data-ttu-id="cb039-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb039-109">-DefaultProfile</span></span>
<span data-ttu-id="cb039-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cb039-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb039-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="cb039-111">-OperationId</span></span>
<span data-ttu-id="cb039-112">Especifica a ID da operação.</span><span class="sxs-lookup"><span data-stu-id="cb039-112">Specifies the operation ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb039-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb039-113">-ResourceGroupName</span></span>
<span data-ttu-id="cb039-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb039-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cb039-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cb039-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="cb039-116">Especifica o nome da configuração de recuperação do sistema do servidor.</span><span class="sxs-lookup"><span data-stu-id="cb039-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="cb039-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="cb039-117">-ServerName</span></span>
<span data-ttu-id="cb039-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="cb039-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="cb039-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb039-119">-Confirm</span></span>
<span data-ttu-id="cb039-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb039-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb039-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb039-121">-WhatIf</span></span>
<span data-ttu-id="cb039-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb039-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb039-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb039-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb039-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb039-124">CommonParameters</span></span>
<span data-ttu-id="cb039-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb039-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb039-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb039-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb039-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb039-127">INPUTS</span></span>

### <span data-ttu-id="cb039-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cb039-128">None</span></span>
<span data-ttu-id="cb039-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cb039-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb039-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb039-130">OUTPUTS</span></span>

## <span data-ttu-id="cb039-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb039-131">NOTES</span></span>

## <span data-ttu-id="cb039-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb039-132">RELATED LINKS</span></span>

[<span data-ttu-id="cb039-133">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="cb039-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
