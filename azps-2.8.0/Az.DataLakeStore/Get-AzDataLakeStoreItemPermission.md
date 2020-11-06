---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596841"
---
# <span data-ttu-id="0bc87-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0bc87-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="0bc87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bc87-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc87-103">Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="0bc87-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0bc87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bc87-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bc87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bc87-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc87-106">O cmdlet **Get-AzDataLakeStoreItemPermission** Obtém a permissão octal de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="0bc87-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0bc87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bc87-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc87-108">Exemplo 1: definir a permissão octal para um arquivo</span><span class="sxs-lookup"><span data-stu-id="0bc87-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="0bc87-109">Esse comando obtém a permissão octal de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0bc87-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="0bc87-110">OS</span><span class="sxs-lookup"><span data-stu-id="0bc87-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc87-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="0bc87-111">-Account</span></span>
<span data-ttu-id="0bc87-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bc87-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="0bc87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc87-113">-DefaultProfile</span></span>
<span data-ttu-id="0bc87-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bc87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bc87-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0bc87-115">-Path</span></span>
<span data-ttu-id="0bc87-116">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="0bc87-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0bc87-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc87-117">CommonParameters</span></span>
<span data-ttu-id="0bc87-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc87-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc87-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc87-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc87-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bc87-120">INPUTS</span></span>

### <span data-ttu-id="0bc87-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc87-121">System.String</span></span>

### <span data-ttu-id="0bc87-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0bc87-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="0bc87-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bc87-123">OUTPUTS</span></span>

### <span data-ttu-id="0bc87-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc87-124">System.String</span></span>

## <span data-ttu-id="0bc87-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bc87-125">NOTES</span></span>
* <span data-ttu-id="0bc87-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0bc87-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="0bc87-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bc87-127">RELATED LINKS</span></span>

[<span data-ttu-id="0bc87-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0bc87-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


