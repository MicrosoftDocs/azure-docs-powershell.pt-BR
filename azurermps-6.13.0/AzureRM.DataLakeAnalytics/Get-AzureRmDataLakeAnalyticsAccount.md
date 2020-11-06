---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 32c7478e7e2419a8f83c839efd841f25446a96c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428503"
---
# <span data-ttu-id="9693c-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9693c-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="9693c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9693c-102">SYNOPSIS</span></span>
<span data-ttu-id="9693c-103">Obtém informações sobre uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9693c-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9693c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9693c-104">SYNTAX</span></span>

### <span data-ttu-id="9693c-105">GetAllInSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="9693c-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9693c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9693c-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9693c-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="9693c-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9693c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9693c-108">DESCRIPTION</span></span>
<span data-ttu-id="9693c-109">O cmdlet **Get-AzureRmDataLakeAnalyticsAccount** Obtém informações sobre uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9693c-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9693c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9693c-110">EXAMPLES</span></span>

### <span data-ttu-id="9693c-111">Exemplo 1: obter informações sobre uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="9693c-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="9693c-112">Esse comando obtém informações sobre a conta chamada ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="9693c-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="9693c-113">OS</span><span class="sxs-lookup"><span data-stu-id="9693c-113">PARAMETERS</span></span>

### <span data-ttu-id="9693c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9693c-114">-DefaultProfile</span></span>
<span data-ttu-id="9693c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9693c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9693c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9693c-116">-Name</span></span>
<span data-ttu-id="9693c-117">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9693c-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9693c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9693c-118">-ResourceGroupName</span></span>
<span data-ttu-id="9693c-119">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9693c-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9693c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9693c-120">CommonParameters</span></span>
<span data-ttu-id="9693c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9693c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9693c-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9693c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9693c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9693c-123">INPUTS</span></span>

### <span data-ttu-id="9693c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9693c-124">System.String</span></span>

## <span data-ttu-id="9693c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9693c-125">OUTPUTS</span></span>

### <span data-ttu-id="9693c-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9693c-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="9693c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9693c-127">NOTES</span></span>

## <span data-ttu-id="9693c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9693c-128">RELATED LINKS</span></span>

[<span data-ttu-id="9693c-129">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9693c-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9693c-130">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9693c-130">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9693c-131">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9693c-131">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9693c-132">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9693c-132">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


