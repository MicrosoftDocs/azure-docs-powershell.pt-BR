---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940499"
---
# <span data-ttu-id="7fec0-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7fec0-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="7fec0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fec0-102">SYNOPSIS</span></span>
<span data-ttu-id="7fec0-103">Obtém uma entrada na ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7fec0-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7fec0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fec0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fec0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fec0-105">DESCRIPTION</span></span>
<span data-ttu-id="7fec0-106">O cmdlet **Get-AzDataLakeStoreItemAclEntry** Obtém uma entrada (ACE) na lista de controle de acesso (ACL) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="7fec0-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7fec0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fec0-107">EXAMPLES</span></span>

### <span data-ttu-id="7fec0-108">Exemplo 1: obter a ACL para uma pasta</span><span class="sxs-lookup"><span data-stu-id="7fec0-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="7fec0-109">Esse comando obtém a ACL para o diretório raiz da conta do repositório do data Lake especificada</span><span class="sxs-lookup"><span data-stu-id="7fec0-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="7fec0-110">OS</span><span class="sxs-lookup"><span data-stu-id="7fec0-110">PARAMETERS</span></span>

### <span data-ttu-id="7fec0-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="7fec0-111">-Account</span></span>
<span data-ttu-id="7fec0-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7fec0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7fec0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fec0-113">-DefaultProfile</span></span>
<span data-ttu-id="7fec0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fec0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fec0-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="7fec0-115">-Path</span></span>
<span data-ttu-id="7fec0-116">Especifica o caminho do repositório data Lake do item para o qual esse cmdlet obtém uma ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="7fec0-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7fec0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fec0-117">CommonParameters</span></span>
<span data-ttu-id="7fec0-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fec0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fec0-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fec0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fec0-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fec0-120">INPUTS</span></span>

### <span data-ttu-id="7fec0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7fec0-121">System.String</span></span>

### <span data-ttu-id="7fec0-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7fec0-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="7fec0-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fec0-123">OUTPUTS</span></span>

### <span data-ttu-id="7fec0-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="7fec0-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="7fec0-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fec0-125">NOTES</span></span>

## <span data-ttu-id="7fec0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fec0-126">RELATED LINKS</span></span>

[<span data-ttu-id="7fec0-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7fec0-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="7fec0-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7fec0-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


