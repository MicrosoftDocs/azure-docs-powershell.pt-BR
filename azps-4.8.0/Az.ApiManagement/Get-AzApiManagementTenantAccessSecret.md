---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955199"
---
# <span data-ttu-id="c6fbd-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="c6fbd-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="c6fbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fbd-103">Obtém as chaves de configuração do Access para um locatário.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="c6fbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6fbd-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6fbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="c6fbd-106">Obtém as chaves de configuração do Access para um locatário.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="c6fbd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="c6fbd-108">Exemplo 1: obter chaves de configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="c6fbd-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="c6fbd-109">Este comando obtém as chaves de configuração de acesso de locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="c6fbd-110">OS</span><span class="sxs-lookup"><span data-stu-id="c6fbd-110">PARAMETERS</span></span>

### <span data-ttu-id="c6fbd-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c6fbd-111">-Context</span></span>
<span data-ttu-id="c6fbd-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c6fbd-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fbd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fbd-114">-DefaultProfile</span></span>
<span data-ttu-id="c6fbd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6fbd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fbd-116">CommonParameters</span></span>
<span data-ttu-id="c6fbd-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6fbd-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6fbd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fbd-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6fbd-119">INPUTS</span></span>

### <span data-ttu-id="c6fbd-120">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c6fbd-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="c6fbd-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6fbd-121">OUTPUTS</span></span>

### <span data-ttu-id="c6fbd-122">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="c6fbd-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="c6fbd-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6fbd-123">NOTES</span></span>

## <span data-ttu-id="c6fbd-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6fbd-124">RELATED LINKS</span></span>
