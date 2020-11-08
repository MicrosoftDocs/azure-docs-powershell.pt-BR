---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112301"
---
# <span data-ttu-id="21245-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="21245-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="21245-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21245-102">SYNOPSIS</span></span>
<span data-ttu-id="21245-103">Testa a existência de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="21245-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="21245-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21245-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21245-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21245-105">DESCRIPTION</span></span>
<span data-ttu-id="21245-106">O cmdlet **Test-AzDataLakeStoreAccount** testa a existência de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="21245-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="21245-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21245-107">EXAMPLES</span></span>

### <span data-ttu-id="21245-108">Exemplo 1: testar uma conta</span><span class="sxs-lookup"><span data-stu-id="21245-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="21245-109">Esse comando testa se a conta denominada ContosoADL existe.</span><span class="sxs-lookup"><span data-stu-id="21245-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="21245-110">OS</span><span class="sxs-lookup"><span data-stu-id="21245-110">PARAMETERS</span></span>

### <span data-ttu-id="21245-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21245-111">-DefaultProfile</span></span>
<span data-ttu-id="21245-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="21245-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21245-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="21245-113">-Name</span></span>
<span data-ttu-id="21245-114">Especifica o nome da conta do data Lake Store para testar.</span><span class="sxs-lookup"><span data-stu-id="21245-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="21245-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21245-115">-ResourceGroupName</span></span>
<span data-ttu-id="21245-116">Especifica o nome do grupo de recursos que contém a conta a ser testada.</span><span class="sxs-lookup"><span data-stu-id="21245-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="21245-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21245-117">CommonParameters</span></span>
<span data-ttu-id="21245-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21245-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21245-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21245-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21245-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21245-120">INPUTS</span></span>

### <span data-ttu-id="21245-121">System. String</span><span class="sxs-lookup"><span data-stu-id="21245-121">System.String</span></span>

## <span data-ttu-id="21245-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21245-122">OUTPUTS</span></span>

### <span data-ttu-id="21245-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21245-123">System.Boolean</span></span>

## <span data-ttu-id="21245-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21245-124">NOTES</span></span>

## <span data-ttu-id="21245-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21245-125">RELATED LINKS</span></span>

[<span data-ttu-id="21245-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="21245-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="21245-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="21245-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="21245-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="21245-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="21245-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="21245-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


