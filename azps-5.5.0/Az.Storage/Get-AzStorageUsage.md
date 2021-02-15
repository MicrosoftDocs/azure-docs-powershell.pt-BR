---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112516"
---
# <span data-ttu-id="1192d-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1192d-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="1192d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1192d-102">SYNOPSIS</span></span>
<span data-ttu-id="1192d-103">Obtém o uso de recursos de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1192d-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="1192d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1192d-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1192d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1192d-105">DESCRIPTION</span></span>
<span data-ttu-id="1192d-106">O cmdlet **Get-AzStorageUsage** obtém o uso do recurso de Armazenamento do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1192d-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="1192d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1192d-107">EXAMPLES</span></span>

### <span data-ttu-id="1192d-108">Exemplo 1: Obter o uso dos recursos de armazenamento do local especificado</span><span class="sxs-lookup"><span data-stu-id="1192d-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="1192d-109">Esse comando obtém o uso de recursos de armazenamento do local especificado sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1192d-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="1192d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1192d-110">PARAMETERS</span></span>

### <span data-ttu-id="1192d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1192d-111">-DefaultProfile</span></span>
<span data-ttu-id="1192d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1192d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1192d-113">-Local</span><span class="sxs-lookup"><span data-stu-id="1192d-113">-Location</span></span>
<span data-ttu-id="1192d-114">Indique para obter o uso de recursos de armazenamento no local especificado.</span><span class="sxs-lookup"><span data-stu-id="1192d-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="1192d-115">Se não especificado, obterá o uso de recursos de armazenamento em todos os locais sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="1192d-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="1192d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1192d-116">CommonParameters</span></span>
<span data-ttu-id="1192d-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1192d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1192d-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1192d-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1192d-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="1192d-119">INPUTS</span></span>

### <span data-ttu-id="1192d-120">System.String</span><span class="sxs-lookup"><span data-stu-id="1192d-120">System.String</span></span>

## <span data-ttu-id="1192d-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="1192d-121">OUTPUTS</span></span>

### <span data-ttu-id="1192d-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="1192d-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="1192d-123">Notas</span><span class="sxs-lookup"><span data-stu-id="1192d-123">NOTES</span></span>

## <span data-ttu-id="1192d-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1192d-124">RELATED LINKS</span></span>

[<span data-ttu-id="1192d-125">Cmdlets do Gerenciador de Armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="1192d-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


