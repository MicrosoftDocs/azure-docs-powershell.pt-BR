---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: d12be29507f581f3e9a8d0de86d8a571a305908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429944"
---
# <span data-ttu-id="7784d-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7784d-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="7784d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7784d-102">SYNOPSIS</span></span>
<span data-ttu-id="7784d-103">Obtém as teclas de acesso para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7784d-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7784d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7784d-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7784d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7784d-105">DESCRIPTION</span></span>
<span data-ttu-id="7784d-106">O cmdlet **Get-AzureRmStorageAccountKey** Obtém as teclas de acesso para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7784d-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="7784d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7784d-107">EXAMPLES</span></span>

### <span data-ttu-id="7784d-108">Exemplo 1: obter as teclas de acesso para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7784d-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="7784d-109">Este comando obtém as chaves da conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="7784d-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="7784d-110">Exemplo 2: obter uma tecla de acesso específica para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7784d-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="7784d-111">OS</span><span class="sxs-lookup"><span data-stu-id="7784d-111">PARAMETERS</span></span>

### <span data-ttu-id="7784d-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="7784d-112">-Name</span></span>
<span data-ttu-id="7784d-113">Especifica o nome da conta de armazenamento para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="7784d-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7784d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7784d-114">-ResourceGroupName</span></span>
<span data-ttu-id="7784d-115">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7784d-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="7784d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7784d-116">-DefaultProfile</span></span>
<span data-ttu-id="7784d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7784d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7784d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7784d-118">CommonParameters</span></span>
<span data-ttu-id="7784d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7784d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7784d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7784d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7784d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7784d-121">INPUTS</span></span>

## <span data-ttu-id="7784d-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7784d-122">OUTPUTS</span></span>

## <span data-ttu-id="7784d-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7784d-123">NOTES</span></span>

## <span data-ttu-id="7784d-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7784d-124">RELATED LINKS</span></span>

[<span data-ttu-id="7784d-125">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7784d-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


