---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4f3ffda3bbac6658cf54af1c7b459ce70f651e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610805"
---
# <span data-ttu-id="95f8f-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="95f8f-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="95f8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="95f8f-103">Verifica a existência de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95f8f-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95f8f-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="95f8f-106">O cmdlet **Test-AzureRmDataLakeAnalyticsAccount** verifica a existência de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95f8f-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="95f8f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95f8f-107">EXAMPLES</span></span>

### <span data-ttu-id="95f8f-108">Exemplo 1: testar se existe uma conta</span><span class="sxs-lookup"><span data-stu-id="95f8f-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="95f8f-109">Esse comando testa se a conta denominada ContosoAdlAccount existe.</span><span class="sxs-lookup"><span data-stu-id="95f8f-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="95f8f-110">OS</span><span class="sxs-lookup"><span data-stu-id="95f8f-110">PARAMETERS</span></span>

### <span data-ttu-id="95f8f-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="95f8f-111">-Name</span></span>
<span data-ttu-id="95f8f-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95f8f-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="95f8f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f8f-113">-ResourceGroupName</span></span>
<span data-ttu-id="95f8f-114">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="95f8f-114">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="95f8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f8f-115">-DefaultProfile</span></span>
<span data-ttu-id="95f8f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95f8f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f8f-117">CommonParameters</span></span>
<span data-ttu-id="95f8f-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f8f-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f8f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f8f-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95f8f-120">INPUTS</span></span>

## <span data-ttu-id="95f8f-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95f8f-121">OUTPUTS</span></span>

### <span data-ttu-id="95f8f-122">bool</span><span class="sxs-lookup"><span data-stu-id="95f8f-122">bool</span></span>
<span data-ttu-id="95f8f-123">True ou false que indica se a conta existe ou não.</span><span class="sxs-lookup"><span data-stu-id="95f8f-123">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="95f8f-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95f8f-124">NOTES</span></span>

## <span data-ttu-id="95f8f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95f8f-125">RELATED LINKS</span></span>

[<span data-ttu-id="95f8f-126">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="95f8f-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="95f8f-127">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="95f8f-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="95f8f-128">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="95f8f-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


