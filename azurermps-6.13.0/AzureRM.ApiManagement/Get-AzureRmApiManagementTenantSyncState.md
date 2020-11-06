---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: c75660c60788d5b2a099be97c927328464f34dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428658"
---
# <span data-ttu-id="57ca4-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="57ca4-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="57ca4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="57ca4-103">Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="57ca4-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57ca4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57ca4-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ca4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57ca4-105">DESCRIPTION</span></span>
<span data-ttu-id="57ca4-106">O cmdlet **Get-AzureRmApiManagementTenantSyncState** Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="57ca4-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="57ca4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57ca4-107">EXAMPLES</span></span>

### <span data-ttu-id="57ca4-108">Exemplo 1: obter o status da sincronização mais recente</span><span class="sxs-lookup"><span data-stu-id="57ca4-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="57ca4-109">Esse comando obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="57ca4-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="57ca4-110">OS</span><span class="sxs-lookup"><span data-stu-id="57ca4-110">PARAMETERS</span></span>

### <span data-ttu-id="57ca4-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="57ca4-111">-Context</span></span>
<span data-ttu-id="57ca4-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="57ca4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="57ca4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ca4-113">-DefaultProfile</span></span>
<span data-ttu-id="57ca4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57ca4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ca4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ca4-115">CommonParameters</span></span>
<span data-ttu-id="57ca4-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ca4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ca4-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ca4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ca4-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57ca4-118">INPUTS</span></span>

### <span data-ttu-id="57ca4-119">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="57ca4-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="57ca4-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57ca4-120">OUTPUTS</span></span>

### <span data-ttu-id="57ca4-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="57ca4-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="57ca4-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57ca4-122">NOTES</span></span>

## <span data-ttu-id="57ca4-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57ca4-123">RELATED LINKS</span></span>
