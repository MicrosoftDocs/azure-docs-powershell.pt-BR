---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433148"
---
# <span data-ttu-id="2d60a-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2d60a-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="2d60a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d60a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d60a-103">Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="2d60a-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d60a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d60a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d60a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d60a-105">DESCRIPTION</span></span>
<span data-ttu-id="2d60a-106">O cmdlet **Get-AzureRmDataLakeStoreItemPermission** Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="2d60a-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2d60a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d60a-107">EXAMPLES</span></span>

### <span data-ttu-id="2d60a-108">Exemplo 1: definir a permissão octal para um arquivo</span><span class="sxs-lookup"><span data-stu-id="2d60a-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="2d60a-109">Esse comando obtém a permissão octal de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d60a-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="2d60a-110">OS</span><span class="sxs-lookup"><span data-stu-id="2d60a-110">PARAMETERS</span></span>

### <span data-ttu-id="2d60a-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="2d60a-111">-Account</span></span>
<span data-ttu-id="2d60a-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d60a-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="2d60a-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2d60a-113">-Path</span></span>
<span data-ttu-id="2d60a-114">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="2d60a-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2d60a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d60a-115">-DefaultProfile</span></span>
<span data-ttu-id="2d60a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d60a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d60a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d60a-117">CommonParameters</span></span>
<span data-ttu-id="2d60a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d60a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d60a-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d60a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d60a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d60a-120">INPUTS</span></span>

## <span data-ttu-id="2d60a-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d60a-121">OUTPUTS</span></span>

### <span data-ttu-id="2d60a-122">String</span><span class="sxs-lookup"><span data-stu-id="2d60a-122">string</span></span>
<span data-ttu-id="2d60a-123">A representação de cadeia de caracteres da propriedade octal</span><span class="sxs-lookup"><span data-stu-id="2d60a-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="2d60a-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d60a-124">NOTES</span></span>
* <span data-ttu-id="2d60a-125">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2d60a-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="2d60a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d60a-126">RELATED LINKS</span></span>

[<span data-ttu-id="2d60a-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2d60a-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


