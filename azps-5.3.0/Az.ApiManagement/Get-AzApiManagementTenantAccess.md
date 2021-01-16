---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432693"
---
# <span data-ttu-id="dd4a2-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="dd4a2-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="dd4a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4a2-103">Obtém a configuração do Access para um locatário.</span><span class="sxs-lookup"><span data-stu-id="dd4a2-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="dd4a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd4a2-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd4a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd4a2-105">DESCRIPTION</span></span>
<span data-ttu-id="dd4a2-106">O cmdlet **Get-AzApiManagementTenantAccess** Obtém a configuração de acesso ao locatário para um locatário.</span><span class="sxs-lookup"><span data-stu-id="dd4a2-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="dd4a2-107">As teclas não serão incluídas nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="dd4a2-107">Keys will not be included into result details.</span></span> <span data-ttu-id="dd4a2-108">Para obter o segredo do cliente, use **Get-AzApiManagementTenantAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="dd4a2-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="dd4a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd4a2-109">EXAMPLES</span></span>

### <span data-ttu-id="dd4a2-110">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="dd4a2-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="dd4a2-111">Este comando obtém a configuração de acesso de locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="dd4a2-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="dd4a2-112">OS</span><span class="sxs-lookup"><span data-stu-id="dd4a2-112">PARAMETERS</span></span>

### <span data-ttu-id="dd4a2-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="dd4a2-113">-Context</span></span>
<span data-ttu-id="dd4a2-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dd4a2-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dd4a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4a2-115">-DefaultProfile</span></span>
<span data-ttu-id="dd4a2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd4a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4a2-117">CommonParameters</span></span>
<span data-ttu-id="dd4a2-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4a2-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd4a2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4a2-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd4a2-120">INPUTS</span></span>

### <span data-ttu-id="dd4a2-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd4a2-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="dd4a2-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd4a2-122">OUTPUTS</span></span>

### <span data-ttu-id="dd4a2-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="dd4a2-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="dd4a2-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd4a2-124">NOTES</span></span>

## <span data-ttu-id="dd4a2-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd4a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="dd4a2-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="dd4a2-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


