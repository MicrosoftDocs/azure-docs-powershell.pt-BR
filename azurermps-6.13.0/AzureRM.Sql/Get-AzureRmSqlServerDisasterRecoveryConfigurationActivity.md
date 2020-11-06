---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 508a19b51fea8435ec48e060e63ee3b3cecc5f65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430005"
---
# <span data-ttu-id="e68ab-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="e68ab-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="e68ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e68ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e68ab-103">Obtém a atividade para uma configuração de recuperação do sistema do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e68ab-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e68ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e68ab-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e68ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e68ab-105">DESCRIPTION</span></span>
<span data-ttu-id="e68ab-106">O cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** Obtém atividade para uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e68ab-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e68ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e68ab-107">EXAMPLES</span></span>

## <span data-ttu-id="e68ab-108">OS</span><span class="sxs-lookup"><span data-stu-id="e68ab-108">PARAMETERS</span></span>

### <span data-ttu-id="e68ab-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68ab-109">-DefaultProfile</span></span>
<span data-ttu-id="e68ab-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e68ab-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e68ab-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e68ab-111">-OperationId</span></span>
<span data-ttu-id="e68ab-112">Especifica a ID da operação.</span><span class="sxs-lookup"><span data-stu-id="e68ab-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ab-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ab-113">-ResourceGroupName</span></span>
<span data-ttu-id="e68ab-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e68ab-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e68ab-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e68ab-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="e68ab-116">Especifica o nome da configuração de recuperação do sistema do servidor.</span><span class="sxs-lookup"><span data-stu-id="e68ab-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="e68ab-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e68ab-117">-ServerName</span></span>
<span data-ttu-id="e68ab-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e68ab-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e68ab-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e68ab-119">-Confirm</span></span>
<span data-ttu-id="e68ab-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e68ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e68ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e68ab-121">-WhatIf</span></span>
<span data-ttu-id="e68ab-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e68ab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e68ab-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e68ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e68ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68ab-124">CommonParameters</span></span>
<span data-ttu-id="e68ab-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e68ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68ab-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e68ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68ab-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e68ab-127">INPUTS</span></span>

### <span data-ttu-id="e68ab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e68ab-128">System.String</span></span>

### <span data-ttu-id="e68ab-129">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e68ab-129">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e68ab-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e68ab-130">OUTPUTS</span></span>

### <span data-ttu-id="e68ab-131">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="e68ab-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="e68ab-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e68ab-132">NOTES</span></span>

## <span data-ttu-id="e68ab-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e68ab-133">RELATED LINKS</span></span>

[<span data-ttu-id="e68ab-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e68ab-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
