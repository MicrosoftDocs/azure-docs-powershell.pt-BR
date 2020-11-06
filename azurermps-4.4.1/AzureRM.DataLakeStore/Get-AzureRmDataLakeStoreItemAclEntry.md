---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609695"
---
# <span data-ttu-id="23abf-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="23abf-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="23abf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23abf-102">SYNOPSIS</span></span>
<span data-ttu-id="23abf-103">Obtém uma entrada na ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23abf-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23abf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23abf-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23abf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23abf-105">DESCRIPTION</span></span>
<span data-ttu-id="23abf-106">O cmdlet **Get-AzureRmDataLakeStoreItemAclEntry** Obtém uma entrada (ACE) na lista de controle de acesso (ACL) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="23abf-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="23abf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23abf-107">EXAMPLES</span></span>

### <span data-ttu-id="23abf-108">Exemplo 1: obter a ACL para uma pasta</span><span class="sxs-lookup"><span data-stu-id="23abf-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="23abf-109">Esse comando obtém a ACL para o diretório raiz da conta do repositório do data Lake especificada</span><span class="sxs-lookup"><span data-stu-id="23abf-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="23abf-110">OS</span><span class="sxs-lookup"><span data-stu-id="23abf-110">PARAMETERS</span></span>

### <span data-ttu-id="23abf-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="23abf-111">-Account</span></span>
<span data-ttu-id="23abf-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23abf-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="23abf-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="23abf-113">-Path</span></span>
<span data-ttu-id="23abf-114">Especifica o caminho do repositório data Lake do item para o qual esse cmdlet obtém uma ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="23abf-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="23abf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23abf-115">-DefaultProfile</span></span>
<span data-ttu-id="23abf-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23abf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23abf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23abf-117">CommonParameters</span></span>
<span data-ttu-id="23abf-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23abf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23abf-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23abf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23abf-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23abf-120">INPUTS</span></span>

## <span data-ttu-id="23abf-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23abf-121">OUTPUTS</span></span>

### <span data-ttu-id="23abf-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="23abf-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="23abf-123">A lista de entradas de ACL para a pasta ou o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="23abf-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="23abf-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23abf-124">NOTES</span></span>

## <span data-ttu-id="23abf-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23abf-125">RELATED LINKS</span></span>

[<span data-ttu-id="23abf-126">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="23abf-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="23abf-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="23abf-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


