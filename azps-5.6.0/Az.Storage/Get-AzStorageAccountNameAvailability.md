---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 6e4582a8963f3d57bacd3dfb9c869368986c5668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891999"
---
# <span data-ttu-id="4158d-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4158d-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="4158d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4158d-102">SYNOPSIS</span></span>
<span data-ttu-id="4158d-103">Verifica a disponibilidade de um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4158d-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="4158d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4158d-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4158d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4158d-105">DESCRIPTION</span></span>
<span data-ttu-id="4158d-106">O cmdlet **Get-AzStorageAccountNameAvailability** verifica se o nome de uma conta de Armazenamento do Azure é válido e está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="4158d-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="4158d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4158d-107">EXAMPLES</span></span>

### <span data-ttu-id="4158d-108">Exemplo 1: Verificar a disponibilidade de um nome de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4158d-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="4158d-109">Este comando verifica a disponibilidade do nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="4158d-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="4158d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4158d-110">PARAMETERS</span></span>

### <span data-ttu-id="4158d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4158d-111">-DefaultProfile</span></span>
<span data-ttu-id="4158d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4158d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4158d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4158d-113">-Name</span></span>
<span data-ttu-id="4158d-114">Especifica o nome da conta de armazenamento que esse cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="4158d-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="4158d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4158d-115">CommonParameters</span></span>
<span data-ttu-id="4158d-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4158d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4158d-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4158d-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4158d-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4158d-118">INPUTS</span></span>

### <span data-ttu-id="4158d-119">System.String</span><span class="sxs-lookup"><span data-stu-id="4158d-119">System.String</span></span>

## <span data-ttu-id="4158d-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4158d-120">OUTPUTS</span></span>

### <span data-ttu-id="4158d-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="4158d-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="4158d-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="4158d-122">NOTES</span></span>

## <span data-ttu-id="4158d-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4158d-123">RELATED LINKS</span></span>

[<span data-ttu-id="4158d-124">Cmdlets do Gerenciador de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="4158d-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


