---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a6e147d64a1dea77febc833b5c46e78d070f3ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427568"
---
# <span data-ttu-id="57fec-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="57fec-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="57fec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57fec-102">SYNOPSIS</span></span>
<span data-ttu-id="57fec-103">Verifica a existência de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="57fec-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57fec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57fec-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57fec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57fec-105">DESCRIPTION</span></span>
<span data-ttu-id="57fec-106">O cmdlet **Test-AzureRmDataLakeAnalyticsAccount** verifica a existência de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="57fec-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="57fec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57fec-107">EXAMPLES</span></span>

### <span data-ttu-id="57fec-108">Exemplo 1: testar se existe uma conta</span><span class="sxs-lookup"><span data-stu-id="57fec-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="57fec-109">Esse comando testa se a conta denominada ContosoAdlAccount existe.</span><span class="sxs-lookup"><span data-stu-id="57fec-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="57fec-110">OS</span><span class="sxs-lookup"><span data-stu-id="57fec-110">PARAMETERS</span></span>

### <span data-ttu-id="57fec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fec-111">-DefaultProfile</span></span>
<span data-ttu-id="57fec-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="57fec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57fec-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="57fec-113">-Name</span></span>
<span data-ttu-id="57fec-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="57fec-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="57fec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fec-115">-ResourceGroupName</span></span>
<span data-ttu-id="57fec-116">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="57fec-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fec-117">CommonParameters</span></span>
<span data-ttu-id="57fec-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57fec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fec-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fec-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fec-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57fec-120">INPUTS</span></span>

### <span data-ttu-id="57fec-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="57fec-121">None</span></span>
<span data-ttu-id="57fec-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="57fec-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57fec-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57fec-123">OUTPUTS</span></span>

### <span data-ttu-id="57fec-124">bool</span><span class="sxs-lookup"><span data-stu-id="57fec-124">bool</span></span>
<span data-ttu-id="57fec-125">True ou false que indica se a conta existe ou não.</span><span class="sxs-lookup"><span data-stu-id="57fec-125">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="57fec-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57fec-126">NOTES</span></span>

## <span data-ttu-id="57fec-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57fec-127">RELATED LINKS</span></span>

[<span data-ttu-id="57fec-128">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="57fec-128">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="57fec-129">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="57fec-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="57fec-130">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="57fec-130">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


