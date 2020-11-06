---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: 64e1d8ad070d4ce1c2f8129a73efd8730f26d1a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429916"
---
# <span data-ttu-id="501aa-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="501aa-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="501aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="501aa-102">SYNOPSIS</span></span>
<span data-ttu-id="501aa-103">Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="501aa-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="501aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="501aa-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="501aa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="501aa-105">DESCRIPTION</span></span>
<span data-ttu-id="501aa-106">O cmdlet **Get-AzureRmApiManagementTenantSyncState** Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="501aa-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="501aa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="501aa-107">EXAMPLES</span></span>

### <span data-ttu-id="501aa-108">Exemplo 1: obter o status da sincronização mais recente</span><span class="sxs-lookup"><span data-stu-id="501aa-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext 
```

<span data-ttu-id="501aa-109">Esse comando obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="501aa-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="501aa-110">OS</span><span class="sxs-lookup"><span data-stu-id="501aa-110">PARAMETERS</span></span>

### <span data-ttu-id="501aa-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="501aa-111">-Context</span></span>
<span data-ttu-id="501aa-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="501aa-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="501aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501aa-113">-DefaultProfile</span></span>
<span data-ttu-id="501aa-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="501aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="501aa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501aa-115">CommonParameters</span></span>
<span data-ttu-id="501aa-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="501aa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501aa-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="501aa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501aa-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="501aa-118">INPUTS</span></span>

### <span data-ttu-id="501aa-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="501aa-119">None</span></span>
<span data-ttu-id="501aa-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="501aa-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="501aa-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="501aa-121">OUTPUTS</span></span>

### <span data-ttu-id="501aa-122">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="501aa-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="501aa-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="501aa-123">NOTES</span></span>

## <span data-ttu-id="501aa-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="501aa-124">RELATED LINKS</span></span>

