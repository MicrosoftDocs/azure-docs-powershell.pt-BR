---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 8c01d617f214df5e505e060d1f0cf1665a9f12bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598087"
---
# <span data-ttu-id="f5f46-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="f5f46-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="f5f46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5f46-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f46-103">Obtém a configuração do Access para um locatário.</span><span class="sxs-lookup"><span data-stu-id="f5f46-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="f5f46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5f46-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5f46-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5f46-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f46-106">O cmdlet **Get-AzApiManagementTenantAccess** Obtém a configuração de acesso ao locatário para um locatário.</span><span class="sxs-lookup"><span data-stu-id="f5f46-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="f5f46-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5f46-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f46-108">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="f5f46-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="f5f46-109">Este comando obtém a configuração de acesso de locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="f5f46-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="f5f46-110">OS</span><span class="sxs-lookup"><span data-stu-id="f5f46-110">PARAMETERS</span></span>

### <span data-ttu-id="f5f46-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f5f46-111">-Context</span></span>
<span data-ttu-id="f5f46-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f5f46-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f5f46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f46-113">-DefaultProfile</span></span>
<span data-ttu-id="f5f46-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5f46-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f46-115">CommonParameters</span></span>
<span data-ttu-id="f5f46-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f46-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f46-117">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5f46-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f46-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5f46-118">INPUTS</span></span>

### <span data-ttu-id="f5f46-119">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f5f46-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="f5f46-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5f46-120">OUTPUTS</span></span>

### <span data-ttu-id="f5f46-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="f5f46-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="f5f46-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5f46-122">NOTES</span></span>

## <span data-ttu-id="f5f46-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5f46-123">RELATED LINKS</span></span>

[<span data-ttu-id="f5f46-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="f5f46-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


