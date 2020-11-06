---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602224"
---
# <span data-ttu-id="1b4a5-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1b4a5-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1b4a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4a5-103">Obtém informações sobre uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b4a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b4a5-104">SYNTAX</span></span>

### <span data-ttu-id="1b4a5-105">Todos na assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b4a5-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b4a5-106">Tudo no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1b4a5-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b4a5-107">Conta específica</span><span class="sxs-lookup"><span data-stu-id="1b4a5-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b4a5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b4a5-108">DESCRIPTION</span></span>
<span data-ttu-id="1b4a5-109">O cmdlet **Get-AzureRmDataLakeAnalyticsAccount** Obtém informações sobre uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1b4a5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b4a5-110">EXAMPLES</span></span>

### <span data-ttu-id="1b4a5-111">Exemplo 1: obter informações sobre uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="1b4a5-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="1b4a5-112">Esse comando obtém informações sobre a conta chamada ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="1b4a5-113">OS</span><span class="sxs-lookup"><span data-stu-id="1b4a5-113">PARAMETERS</span></span>

### <span data-ttu-id="1b4a5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b4a5-114">-Name</span></span>
<span data-ttu-id="1b4a5-115">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b4a5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4a5-116">-ResourceGroupName</span></span>
<span data-ttu-id="1b4a5-117">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b4a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4a5-118">-DefaultProfile</span></span>
<span data-ttu-id="1b4a5-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b4a5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4a5-120">CommonParameters</span></span>
<span data-ttu-id="1b4a5-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4a5-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b4a5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4a5-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b4a5-123">INPUTS</span></span>

## <span data-ttu-id="1b4a5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b4a5-124">OUTPUTS</span></span>

### <span data-ttu-id="1b4a5-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1b4a5-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="1b4a5-126">Os detalhes da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-126">The specified account details.</span></span>

### <span data-ttu-id="1b4a5-127">Programação<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="1b4a5-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="1b4a5-128">A lista de contas no grupo de recursos ou na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="1b4a5-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="1b4a5-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b4a5-129">NOTES</span></span>

## <span data-ttu-id="1b4a5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b4a5-130">RELATED LINKS</span></span>

[<span data-ttu-id="1b4a5-131">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1b4a5-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1b4a5-132">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1b4a5-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1b4a5-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1b4a5-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1b4a5-134">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1b4a5-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


