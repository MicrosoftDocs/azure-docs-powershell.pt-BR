---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955652"
---
# <span data-ttu-id="e6f2a-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e6f2a-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e6f2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f2a-103">Obtém informações sobre uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e6f2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6f2a-104">SYNTAX</span></span>

### <span data-ttu-id="e6f2a-105">GetAllInSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6f2a-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6f2a-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6f2a-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6f2a-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="e6f2a-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6f2a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6f2a-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f2a-109">O cmdlet **Get-AzDataLakeAnalyticsAccount** Obtém informações sobre uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e6f2a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6f2a-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f2a-111">Exemplo 1: obter informações sobre uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="e6f2a-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="e6f2a-112">Esse comando obtém informações sobre a conta chamada ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="e6f2a-113">OS</span><span class="sxs-lookup"><span data-stu-id="e6f2a-113">PARAMETERS</span></span>

### <span data-ttu-id="e6f2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f2a-114">-DefaultProfile</span></span>
<span data-ttu-id="e6f2a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e6f2a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f2a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6f2a-116">-Name</span></span>
<span data-ttu-id="e6f2a-117">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e6f2a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f2a-118">-ResourceGroupName</span></span>
<span data-ttu-id="e6f2a-119">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e6f2a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f2a-120">CommonParameters</span></span>
<span data-ttu-id="e6f2a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f2a-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f2a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f2a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6f2a-123">INPUTS</span></span>

### <span data-ttu-id="e6f2a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f2a-124">System.String</span></span>

## <span data-ttu-id="e6f2a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6f2a-125">OUTPUTS</span></span>

### <span data-ttu-id="e6f2a-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e6f2a-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="e6f2a-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="e6f2a-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="e6f2a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6f2a-128">NOTES</span></span>

## <span data-ttu-id="e6f2a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6f2a-129">RELATED LINKS</span></span>

[<span data-ttu-id="e6f2a-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e6f2a-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e6f2a-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e6f2a-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e6f2a-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e6f2a-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e6f2a-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e6f2a-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


