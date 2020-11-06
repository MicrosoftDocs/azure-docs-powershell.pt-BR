---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: e527501424edfbbc12693b47b5858c3c46592402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602961"
---
# <span data-ttu-id="6401a-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6401a-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="6401a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6401a-102">SYNOPSIS</span></span>
<span data-ttu-id="6401a-103">Verifica a existência de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6401a-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6401a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6401a-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6401a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6401a-105">DESCRIPTION</span></span>
<span data-ttu-id="6401a-106">O cmdlet **Test-AzureRmDataLakeAnalyticsAccount** verifica a existência de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6401a-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6401a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6401a-107">EXAMPLES</span></span>

### <span data-ttu-id="6401a-108">Exemplo 1: testar se existe uma conta</span><span class="sxs-lookup"><span data-stu-id="6401a-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="6401a-109">Esse comando testa se a conta denominada ContosoAdlAccount existe.</span><span class="sxs-lookup"><span data-stu-id="6401a-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="6401a-110">OS</span><span class="sxs-lookup"><span data-stu-id="6401a-110">PARAMETERS</span></span>

### <span data-ttu-id="6401a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6401a-111">-DefaultProfile</span></span>
<span data-ttu-id="6401a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6401a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6401a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6401a-113">-Name</span></span>
<span data-ttu-id="6401a-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6401a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6401a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6401a-115">-ResourceGroupName</span></span>
<span data-ttu-id="6401a-116">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6401a-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6401a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6401a-117">CommonParameters</span></span>
<span data-ttu-id="6401a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6401a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6401a-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6401a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6401a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6401a-120">INPUTS</span></span>

### <span data-ttu-id="6401a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6401a-121">System.String</span></span>

## <span data-ttu-id="6401a-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6401a-122">OUTPUTS</span></span>

### <span data-ttu-id="6401a-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6401a-123">System.Boolean</span></span>

## <span data-ttu-id="6401a-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6401a-124">NOTES</span></span>

## <span data-ttu-id="6401a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6401a-125">RELATED LINKS</span></span>

[<span data-ttu-id="6401a-126">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6401a-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6401a-127">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6401a-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6401a-128">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6401a-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


