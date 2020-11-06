---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 0e1182843ee57809fe3c6a0ed1c7f516678fc1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429809"
---
# <span data-ttu-id="b9441-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9441-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="b9441-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9441-102">SYNOPSIS</span></span>
<span data-ttu-id="b9441-103">Obtém uma entrada na ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b9441-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9441-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9441-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9441-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9441-105">DESCRIPTION</span></span>
<span data-ttu-id="b9441-106">O cmdlet **Get-AzureRmDataLakeStoreItemAclEntry** Obtém uma entrada (ACE) na lista de controle de acesso (ACL) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="b9441-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b9441-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9441-107">EXAMPLES</span></span>

### <span data-ttu-id="b9441-108">Exemplo 1: obter a ACL para uma pasta</span><span class="sxs-lookup"><span data-stu-id="b9441-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="b9441-109">Esse comando obtém a ACL para o diretório raiz da conta do repositório do data Lake especificada</span><span class="sxs-lookup"><span data-stu-id="b9441-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="b9441-110">OS</span><span class="sxs-lookup"><span data-stu-id="b9441-110">PARAMETERS</span></span>

### <span data-ttu-id="b9441-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="b9441-111">-Account</span></span>
<span data-ttu-id="b9441-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b9441-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9441-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9441-113">-DefaultProfile</span></span>
<span data-ttu-id="b9441-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9441-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9441-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b9441-115">-Path</span></span>
<span data-ttu-id="b9441-116">Especifica o caminho do repositório data Lake do item para o qual esse cmdlet obtém uma ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="b9441-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9441-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9441-117">CommonParameters</span></span>
<span data-ttu-id="b9441-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9441-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9441-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9441-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9441-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9441-120">INPUTS</span></span>

### <span data-ttu-id="b9441-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b9441-121">None</span></span>
<span data-ttu-id="b9441-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b9441-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9441-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9441-123">OUTPUTS</span></span>

### <span data-ttu-id="b9441-124">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="b9441-124">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="b9441-125">A lista de entradas de ACL para a pasta ou o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b9441-125">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="b9441-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9441-126">NOTES</span></span>

## <span data-ttu-id="b9441-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9441-127">RELATED LINKS</span></span>

[<span data-ttu-id="b9441-128">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9441-128">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="b9441-129">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9441-129">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


