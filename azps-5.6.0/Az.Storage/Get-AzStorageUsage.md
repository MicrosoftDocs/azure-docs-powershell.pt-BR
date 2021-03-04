---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 9e12aa08bd37a5dfa467b2df03df42f5c58e4186
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890919"
---
# <span data-ttu-id="8660b-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8660b-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="8660b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8660b-102">SYNOPSIS</span></span>
<span data-ttu-id="8660b-103">Obtém o uso de recursos de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8660b-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="8660b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8660b-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8660b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8660b-105">DESCRIPTION</span></span>
<span data-ttu-id="8660b-106">O cmdlet **Get-AzStorageUsage** obtém o uso de recursos para o Armazenamento do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8660b-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="8660b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8660b-107">EXAMPLES</span></span>

### <span data-ttu-id="8660b-108">Exemplo 1: Obter o uso de recursos de armazenamento do local especificado</span><span class="sxs-lookup"><span data-stu-id="8660b-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="8660b-109">Este comando obtém o uso de recursos de armazenamento do local especificado na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8660b-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="8660b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8660b-110">PARAMETERS</span></span>

### <span data-ttu-id="8660b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8660b-111">-DefaultProfile</span></span>
<span data-ttu-id="8660b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8660b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8660b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8660b-113">-Location</span></span>
<span data-ttu-id="8660b-114">Indique para obter o uso de recursos de armazenamento no local especificado.</span><span class="sxs-lookup"><span data-stu-id="8660b-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="8660b-115">Se não for especificado, obterá o uso de recursos de armazenamento em todos os locais sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="8660b-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8660b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8660b-116">CommonParameters</span></span>
<span data-ttu-id="8660b-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8660b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8660b-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8660b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8660b-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8660b-119">INPUTS</span></span>

### <span data-ttu-id="8660b-120">System.String</span><span class="sxs-lookup"><span data-stu-id="8660b-120">System.String</span></span>

## <span data-ttu-id="8660b-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8660b-121">OUTPUTS</span></span>

### <span data-ttu-id="8660b-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="8660b-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="8660b-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="8660b-123">NOTES</span></span>

## <span data-ttu-id="8660b-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8660b-124">RELATED LINKS</span></span>

[<span data-ttu-id="8660b-125">Cmdlets do Gerenciador de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="8660b-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


