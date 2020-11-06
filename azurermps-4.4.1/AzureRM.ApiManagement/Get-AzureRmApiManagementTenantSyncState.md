---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: b9d7426bf275571d025ec0fef3f8bbec7c119c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440235"
---
# <span data-ttu-id="306b0-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="306b0-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="306b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="306b0-102">SYNOPSIS</span></span>
<span data-ttu-id="306b0-103">Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="306b0-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="306b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="306b0-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="306b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="306b0-105">DESCRIPTION</span></span>
<span data-ttu-id="306b0-106">O cmdlet **Get-AzureRmApiManagementTenantSyncState** Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="306b0-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="306b0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="306b0-107">EXAMPLES</span></span>

### <span data-ttu-id="306b0-108">Exemplo 1: obter o status da sincronização mais recente</span><span class="sxs-lookup"><span data-stu-id="306b0-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $ApimContext
```

<span data-ttu-id="306b0-109">Esse comando obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="306b0-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="306b0-110">OS</span><span class="sxs-lookup"><span data-stu-id="306b0-110">PARAMETERS</span></span>

### <span data-ttu-id="306b0-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="306b0-111">-Context</span></span>
<span data-ttu-id="306b0-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="306b0-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="306b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306b0-113">-DefaultProfile</span></span>
<span data-ttu-id="306b0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="306b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="306b0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306b0-115">CommonParameters</span></span>
<span data-ttu-id="306b0-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="306b0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306b0-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="306b0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306b0-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="306b0-118">INPUTS</span></span>

## <span data-ttu-id="306b0-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="306b0-119">OUTPUTS</span></span>

### <span data-ttu-id="306b0-120">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="306b0-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="306b0-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="306b0-121">NOTES</span></span>

## <span data-ttu-id="306b0-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="306b0-122">RELATED LINKS</span></span>

