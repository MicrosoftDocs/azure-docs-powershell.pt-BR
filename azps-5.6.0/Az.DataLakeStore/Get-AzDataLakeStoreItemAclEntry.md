---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 76d745c16dae7fdfae7feca46c3b32715fa82f5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890861"
---
# <span data-ttu-id="d11c7-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d11c7-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d11c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d11c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d11c7-103">Obtém uma entrada na ACL de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d11c7-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d11c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d11c7-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d11c7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d11c7-105">DESCRIPTION</span></span>
<span data-ttu-id="d11c7-106">O cmdlet **Get-AzDataLakeStoreItemAclEntry** obtém uma entrada (ACE) na lista de controle de acesso (ACL) de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d11c7-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d11c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d11c7-107">EXAMPLES</span></span>

### <span data-ttu-id="d11c7-108">Exemplo 1: Obter a ACL para uma pasta</span><span class="sxs-lookup"><span data-stu-id="d11c7-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="d11c7-109">Este comando obtém a ACL para o diretório raiz da conta do Data Lake Store especificada</span><span class="sxs-lookup"><span data-stu-id="d11c7-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="d11c7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d11c7-110">PARAMETERS</span></span>

### <span data-ttu-id="d11c7-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d11c7-111">-Account</span></span>
<span data-ttu-id="d11c7-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d11c7-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d11c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11c7-113">-DefaultProfile</span></span>
<span data-ttu-id="d11c7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d11c7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d11c7-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d11c7-115">-Path</span></span>
<span data-ttu-id="d11c7-116">Especifica o caminho do Data Lake Store do item para o qual este cmdlet obtém um ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="d11c7-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d11c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11c7-117">CommonParameters</span></span>
<span data-ttu-id="d11c7-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11c7-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d11c7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11c7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d11c7-120">INPUTS</span></span>

### <span data-ttu-id="d11c7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d11c7-121">System.String</span></span>

### <span data-ttu-id="d11c7-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d11c7-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d11c7-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d11c7-123">OUTPUTS</span></span>

### <span data-ttu-id="d11c7-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="d11c7-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="d11c7-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="d11c7-125">NOTES</span></span>

## <span data-ttu-id="d11c7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d11c7-126">RELATED LINKS</span></span>

[<span data-ttu-id="d11c7-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d11c7-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="d11c7-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d11c7-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


