---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113266"
---
# <span data-ttu-id="dbecd-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dbecd-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="dbecd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbecd-102">SYNOPSIS</span></span>
<span data-ttu-id="dbecd-103">Obtém informações sobre uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dbecd-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="dbecd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbecd-104">SYNTAX</span></span>

### <span data-ttu-id="dbecd-105">GetAllInSubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dbecd-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbecd-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dbecd-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbecd-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="dbecd-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbecd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbecd-108">DESCRIPTION</span></span>
<span data-ttu-id="dbecd-109">O cmdlet **Get-AzDataLakeAnalyticsAccount** obtém informações sobre uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dbecd-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="dbecd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dbecd-110">EXAMPLES</span></span>

### <span data-ttu-id="dbecd-111">Exemplo 1: obter informações sobre uma conta do Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="dbecd-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="dbecd-112">Este comando obtém informações sobre a conta chamada ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="dbecd-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="dbecd-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbecd-113">PARAMETERS</span></span>

### <span data-ttu-id="dbecd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbecd-114">-DefaultProfile</span></span>
<span data-ttu-id="dbecd-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dbecd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbecd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbecd-116">-Name</span></span>
<span data-ttu-id="dbecd-117">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dbecd-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="dbecd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbecd-118">-ResourceGroupName</span></span>
<span data-ttu-id="dbecd-119">Especifica o nome do grupo de recursos da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dbecd-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="dbecd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbecd-120">CommonParameters</span></span>
<span data-ttu-id="dbecd-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbecd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbecd-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbecd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbecd-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="dbecd-123">INPUTS</span></span>

### <span data-ttu-id="dbecd-124">System.String</span><span class="sxs-lookup"><span data-stu-id="dbecd-124">System.String</span></span>

## <span data-ttu-id="dbecd-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="dbecd-125">OUTPUTS</span></span>

### <span data-ttu-id="dbecd-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dbecd-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="dbecd-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="dbecd-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="dbecd-128">Notas</span><span class="sxs-lookup"><span data-stu-id="dbecd-128">NOTES</span></span>

## <span data-ttu-id="dbecd-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbecd-129">RELATED LINKS</span></span>

[<span data-ttu-id="dbecd-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dbecd-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="dbecd-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dbecd-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="dbecd-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dbecd-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="dbecd-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dbecd-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


