---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bc8a09add012cb0f190922777e2e9e7fcc46feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891033"
---
# <span data-ttu-id="0f4f1-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4f1-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="0f4f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4f1-103">Testa a existência de uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f4f1-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="0f4f1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0f4f1-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4f1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0f4f1-105">DESCRIPTION</span></span>
<span data-ttu-id="0f4f1-106">O cmdlet **Test-AzDataLakeStoreAccount** testa a existência de uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f4f1-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="0f4f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f4f1-107">EXAMPLES</span></span>

### <span data-ttu-id="0f4f1-108">Exemplo 1: Testar uma conta</span><span class="sxs-lookup"><span data-stu-id="0f4f1-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="0f4f1-109">Este comando testa se a conta chamada ContosoADL existe.</span><span class="sxs-lookup"><span data-stu-id="0f4f1-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="0f4f1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0f4f1-110">PARAMETERS</span></span>

### <span data-ttu-id="0f4f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4f1-111">-DefaultProfile</span></span>
<span data-ttu-id="0f4f1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0f4f1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f4f1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0f4f1-113">-Name</span></span>
<span data-ttu-id="0f4f1-114">Especifica o nome da conta do Data Lake Store a ser testado.</span><span class="sxs-lookup"><span data-stu-id="0f4f1-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="0f4f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f4f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f4f1-116">Especifica o nome do grupo de recursos que contém a conta a ser testado.</span><span class="sxs-lookup"><span data-stu-id="0f4f1-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="0f4f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4f1-117">CommonParameters</span></span>
<span data-ttu-id="0f4f1-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f4f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4f1-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4f1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4f1-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f4f1-120">INPUTS</span></span>

### <span data-ttu-id="0f4f1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0f4f1-121">System.String</span></span>

## <span data-ttu-id="0f4f1-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0f4f1-122">OUTPUTS</span></span>

### <span data-ttu-id="0f4f1-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f4f1-123">System.Boolean</span></span>

## <span data-ttu-id="0f4f1-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="0f4f1-124">NOTES</span></span>

## <span data-ttu-id="0f4f1-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f4f1-125">RELATED LINKS</span></span>

[<span data-ttu-id="0f4f1-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4f1-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0f4f1-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4f1-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0f4f1-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4f1-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0f4f1-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0f4f1-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


