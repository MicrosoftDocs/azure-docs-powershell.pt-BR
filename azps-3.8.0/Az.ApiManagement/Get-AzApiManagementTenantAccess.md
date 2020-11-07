---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 3c4151cbc6b170f8b34e70126f37e4478933744d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940932"
---
# <span data-ttu-id="c9e4c-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="c9e4c-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="c9e4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e4c-103">Obtém a configuração do Access para um locatário.</span><span class="sxs-lookup"><span data-stu-id="c9e4c-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="c9e4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9e4c-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9e4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9e4c-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e4c-106">O cmdlet **Get-AzApiManagementTenantAccess** Obtém a configuração de acesso ao locatário para um locatário.</span><span class="sxs-lookup"><span data-stu-id="c9e4c-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="c9e4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9e4c-107">EXAMPLES</span></span>

### <span data-ttu-id="c9e4c-108">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="c9e4c-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="c9e4c-109">Este comando obtém a configuração de acesso de locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="c9e4c-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="c9e4c-110">OS</span><span class="sxs-lookup"><span data-stu-id="c9e4c-110">PARAMETERS</span></span>

### <span data-ttu-id="c9e4c-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c9e4c-111">-Context</span></span>
<span data-ttu-id="c9e4c-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c9e4c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c9e4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e4c-113">-DefaultProfile</span></span>
<span data-ttu-id="c9e4c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9e4c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e4c-115">CommonParameters</span></span>
<span data-ttu-id="c9e4c-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e4c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e4c-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9e4c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e4c-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9e4c-118">INPUTS</span></span>

### <span data-ttu-id="c9e4c-119">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9e4c-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="c9e4c-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9e4c-120">OUTPUTS</span></span>

### <span data-ttu-id="c9e4c-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="c9e4c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="c9e4c-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9e4c-122">NOTES</span></span>

## <span data-ttu-id="c9e4c-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9e4c-123">RELATED LINKS</span></span>

[<span data-ttu-id="c9e4c-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="c9e4c-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


