---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113643"
---
# <span data-ttu-id="3ef69-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="3ef69-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="3ef69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ef69-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef69-103">Obtém as teclas de configuração de acesso para um locatário.</span><span class="sxs-lookup"><span data-stu-id="3ef69-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="3ef69-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ef69-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ef69-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ef69-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef69-106">Obtém as teclas de configuração de acesso para um locatário.</span><span class="sxs-lookup"><span data-stu-id="3ef69-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="3ef69-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ef69-107">EXAMPLES</span></span>

### <span data-ttu-id="3ef69-108">Exemplo 1: Obter teclas de configuração de acesso do locatário</span><span class="sxs-lookup"><span data-stu-id="3ef69-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="3ef69-109">Esse comando obtém as teclas de configuração de acesso do locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="3ef69-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="3ef69-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ef69-110">PARAMETERS</span></span>

### <span data-ttu-id="3ef69-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3ef69-111">-Context</span></span>
<span data-ttu-id="3ef69-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3ef69-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3ef69-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3ef69-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3ef69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef69-114">-DefaultProfile</span></span>
<span data-ttu-id="3ef69-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef69-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef69-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef69-116">CommonParameters</span></span>
<span data-ttu-id="3ef69-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef69-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef69-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ef69-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef69-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="3ef69-119">INPUTS</span></span>

### <span data-ttu-id="3ef69-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ef69-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3ef69-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="3ef69-121">OUTPUTS</span></span>

### <span data-ttu-id="3ef69-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3ef69-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3ef69-123">Notas</span><span class="sxs-lookup"><span data-stu-id="3ef69-123">NOTES</span></span>

## <span data-ttu-id="3ef69-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ef69-124">RELATED LINKS</span></span>
