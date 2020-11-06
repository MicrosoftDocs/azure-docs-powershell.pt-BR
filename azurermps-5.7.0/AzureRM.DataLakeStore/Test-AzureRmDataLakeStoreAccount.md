---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 15c0614094ed28a9888e2e39a6cfb81547fbb6e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439890"
---
# <span data-ttu-id="9ae9d-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ae9d-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="9ae9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ae9d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae9d-103">Testa a existência de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ae9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ae9d-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ae9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ae9d-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae9d-106">O cmdlet **Test-AzureRmDataLakeStoreAccount** testa a existência de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="9ae9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ae9d-107">EXAMPLES</span></span>

### <span data-ttu-id="9ae9d-108">Exemplo 1: testar uma conta</span><span class="sxs-lookup"><span data-stu-id="9ae9d-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="9ae9d-109">Esse comando testa se a conta denominada ContosoADL existe.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="9ae9d-110">OS</span><span class="sxs-lookup"><span data-stu-id="9ae9d-110">PARAMETERS</span></span>

### <span data-ttu-id="9ae9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae9d-111">-DefaultProfile</span></span>
<span data-ttu-id="9ae9d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9ae9d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ae9d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ae9d-113">-Name</span></span>
<span data-ttu-id="9ae9d-114">Especifica o nome da conta do data Lake Store para testar.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="9ae9d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae9d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ae9d-116">Especifica o nome do grupo de recursos que contém a conta a ser testada.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="9ae9d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae9d-117">CommonParameters</span></span>
<span data-ttu-id="9ae9d-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae9d-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae9d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae9d-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ae9d-120">INPUTS</span></span>

### <span data-ttu-id="9ae9d-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9ae9d-121">None</span></span>
<span data-ttu-id="9ae9d-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ae9d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ae9d-123">OUTPUTS</span></span>

### <span data-ttu-id="9ae9d-124">bool</span><span class="sxs-lookup"><span data-stu-id="9ae9d-124">bool</span></span>
<span data-ttu-id="9ae9d-125">True ou false que indica a existência da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="9ae9d-125">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="9ae9d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ae9d-126">NOTES</span></span>

## <span data-ttu-id="9ae9d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ae9d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9ae9d-128">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ae9d-128">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9ae9d-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ae9d-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9ae9d-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ae9d-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="9ae9d-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9ae9d-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


