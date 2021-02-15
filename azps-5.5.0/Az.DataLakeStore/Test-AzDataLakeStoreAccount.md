---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111940"
---
# <span data-ttu-id="0b2bc-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0b2bc-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="0b2bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2bc-103">Testa a existência de uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="0b2bc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b2bc-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b2bc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="0b2bc-106">O cmdlet **Test-AzDataLakeStoreAccount** testa a existência de uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="0b2bc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b2bc-107">EXAMPLES</span></span>

### <span data-ttu-id="0b2bc-108">Exemplo 1: Testar uma conta</span><span class="sxs-lookup"><span data-stu-id="0b2bc-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="0b2bc-109">Esse comando testa se a conta chamada ContosoADL existe.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="0b2bc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b2bc-110">PARAMETERS</span></span>

### <span data-ttu-id="0b2bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2bc-111">-DefaultProfile</span></span>
<span data-ttu-id="0b2bc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0b2bc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b2bc-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b2bc-113">-Name</span></span>
<span data-ttu-id="0b2bc-114">Especifica o nome da conta do Data Lake Store a ser testado.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="0b2bc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2bc-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b2bc-116">Especifica o nome do grupo de recursos que contém a conta a ser testado.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="0b2bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2bc-117">CommonParameters</span></span>
<span data-ttu-id="0b2bc-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2bc-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2bc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2bc-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b2bc-120">INPUTS</span></span>

### <span data-ttu-id="0b2bc-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0b2bc-121">System.String</span></span>

## <span data-ttu-id="0b2bc-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b2bc-122">OUTPUTS</span></span>

### <span data-ttu-id="0b2bc-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b2bc-123">System.Boolean</span></span>

## <span data-ttu-id="0b2bc-124">Notas</span><span class="sxs-lookup"><span data-stu-id="0b2bc-124">NOTES</span></span>

## <span data-ttu-id="0b2bc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b2bc-125">RELATED LINKS</span></span>

[<span data-ttu-id="0b2bc-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0b2bc-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0b2bc-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0b2bc-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0b2bc-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0b2bc-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0b2bc-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0b2bc-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


