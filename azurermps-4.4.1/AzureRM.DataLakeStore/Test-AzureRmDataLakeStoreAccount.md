---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 8aeb682b270de821a6944c619d7933148b2855e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441117"
---
# <span data-ttu-id="28a16-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="28a16-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="28a16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28a16-102">SYNOPSIS</span></span>
<span data-ttu-id="28a16-103">Testa a existência de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="28a16-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28a16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28a16-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a16-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28a16-105">DESCRIPTION</span></span>
<span data-ttu-id="28a16-106">O cmdlet **Test-AzureRmDataLakeStoreAccount** testa a existência de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="28a16-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="28a16-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28a16-107">EXAMPLES</span></span>

### <span data-ttu-id="28a16-108">Exemplo 1: testar uma conta</span><span class="sxs-lookup"><span data-stu-id="28a16-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="28a16-109">Esse comando testa se a conta denominada ContosoADL existe.</span><span class="sxs-lookup"><span data-stu-id="28a16-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="28a16-110">OS</span><span class="sxs-lookup"><span data-stu-id="28a16-110">PARAMETERS</span></span>

### <span data-ttu-id="28a16-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="28a16-111">-Name</span></span>
<span data-ttu-id="28a16-112">Especifica o nome da conta do data Lake Store para testar.</span><span class="sxs-lookup"><span data-stu-id="28a16-112">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="28a16-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a16-113">-ResourceGroupName</span></span>
<span data-ttu-id="28a16-114">Especifica o nome do grupo de recursos que contém a conta a ser testada.</span><span class="sxs-lookup"><span data-stu-id="28a16-114">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="28a16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a16-115">-DefaultProfile</span></span>
<span data-ttu-id="28a16-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28a16-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28a16-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a16-117">CommonParameters</span></span>
<span data-ttu-id="28a16-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a16-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a16-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a16-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a16-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28a16-120">INPUTS</span></span>

## <span data-ttu-id="28a16-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28a16-121">OUTPUTS</span></span>

### <span data-ttu-id="28a16-122">bool</span><span class="sxs-lookup"><span data-stu-id="28a16-122">bool</span></span>
<span data-ttu-id="28a16-123">True ou false que indica a existência da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="28a16-123">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="28a16-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28a16-124">NOTES</span></span>

## <span data-ttu-id="28a16-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28a16-125">RELATED LINKS</span></span>

[<span data-ttu-id="28a16-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="28a16-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="28a16-127">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="28a16-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="28a16-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="28a16-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="28a16-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="28a16-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

