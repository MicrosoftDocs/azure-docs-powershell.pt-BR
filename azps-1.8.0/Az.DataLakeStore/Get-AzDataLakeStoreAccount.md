---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: b06b64b81679d1f0f9429be0362f936046e54ee5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770943"
---
# <span data-ttu-id="91dce-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="91dce-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="91dce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91dce-102">SYNOPSIS</span></span>
<span data-ttu-id="91dce-103">Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="91dce-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="91dce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91dce-104">SYNTAX</span></span>

### <span data-ttu-id="91dce-105">GetAllInSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="91dce-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91dce-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91dce-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91dce-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="91dce-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91dce-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91dce-108">DESCRIPTION</span></span>
<span data-ttu-id="91dce-109">O cmdlet **Get-AzDataLakeStoreAccount** Obtém detalhes de uma conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="91dce-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="91dce-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91dce-110">EXAMPLES</span></span>

### <span data-ttu-id="91dce-111">Exemplo 1: obter uma conta do data Lake Store</span><span class="sxs-lookup"><span data-stu-id="91dce-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="91dce-112">Esse comando obtém a conta chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="91dce-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="91dce-113">OS</span><span class="sxs-lookup"><span data-stu-id="91dce-113">PARAMETERS</span></span>

### <span data-ttu-id="91dce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91dce-114">-DefaultProfile</span></span>
<span data-ttu-id="91dce-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="91dce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91dce-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="91dce-116">-Name</span></span>
<span data-ttu-id="91dce-117">Especifica o nome da conta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="91dce-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="91dce-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91dce-118">-ResourceGroupName</span></span>
<span data-ttu-id="91dce-119">Especifica o nome do grupo de recursos que contém a conta do data Lake Store a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="91dce-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="91dce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91dce-120">CommonParameters</span></span>
<span data-ttu-id="91dce-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91dce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91dce-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91dce-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91dce-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91dce-123">INPUTS</span></span>

### <span data-ttu-id="91dce-124">System. String</span><span class="sxs-lookup"><span data-stu-id="91dce-124">System.String</span></span>

## <span data-ttu-id="91dce-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91dce-125">OUTPUTS</span></span>

### <span data-ttu-id="91dce-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="91dce-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="91dce-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91dce-127">NOTES</span></span>

## <span data-ttu-id="91dce-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91dce-128">RELATED LINKS</span></span>

[<span data-ttu-id="91dce-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="91dce-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="91dce-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="91dce-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="91dce-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="91dce-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="91dce-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="91dce-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


