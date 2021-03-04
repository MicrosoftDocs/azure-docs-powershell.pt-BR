---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 845fbb645ca9ba3495aa0dcf2b56cdbd793630e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886773"
---
# <span data-ttu-id="5bfd3-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5bfd3-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="5bfd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bfd3-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfd3-103">Obtém detalhes de uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5bfd3-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="5bfd3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5bfd3-104">SYNTAX</span></span>

### <span data-ttu-id="5bfd3-105">GetAllInSubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5bfd3-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bfd3-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5bfd3-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bfd3-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="5bfd3-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bfd3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5bfd3-108">DESCRIPTION</span></span>
<span data-ttu-id="5bfd3-109">O cmdlet **Get-AzDataLakeStoreAccount** obtém detalhes de uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5bfd3-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="5bfd3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bfd3-110">EXAMPLES</span></span>

### <span data-ttu-id="5bfd3-111">Exemplo 1: Obter uma conta do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5bfd3-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="5bfd3-112">Este comando obtém a conta chamada ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="5bfd3-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="5bfd3-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5bfd3-113">PARAMETERS</span></span>

### <span data-ttu-id="5bfd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bfd3-114">-DefaultProfile</span></span>
<span data-ttu-id="5bfd3-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5bfd3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bfd3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5bfd3-116">-Name</span></span>
<span data-ttu-id="5bfd3-117">Especifica o nome da conta a ser obter.</span><span class="sxs-lookup"><span data-stu-id="5bfd3-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="5bfd3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bfd3-118">-ResourceGroupName</span></span>
<span data-ttu-id="5bfd3-119">Especifica o nome do grupo de recursos que contém a conta do Data Lake Store para obter.</span><span class="sxs-lookup"><span data-stu-id="5bfd3-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="5bfd3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfd3-120">CommonParameters</span></span>
<span data-ttu-id="5bfd3-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bfd3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfd3-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bfd3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfd3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bfd3-123">INPUTS</span></span>

### <span data-ttu-id="5bfd3-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5bfd3-124">System.String</span></span>

## <span data-ttu-id="5bfd3-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5bfd3-125">OUTPUTS</span></span>

### <span data-ttu-id="5bfd3-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5bfd3-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="5bfd3-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="5bfd3-127">NOTES</span></span>

## <span data-ttu-id="5bfd3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bfd3-128">RELATED LINKS</span></span>

[<span data-ttu-id="5bfd3-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5bfd3-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5bfd3-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5bfd3-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5bfd3-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5bfd3-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5bfd3-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5bfd3-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


