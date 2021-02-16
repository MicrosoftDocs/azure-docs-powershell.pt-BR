---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113644"
---
# <span data-ttu-id="5a273-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5a273-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="5a273-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a273-102">SYNOPSIS</span></span>
<span data-ttu-id="5a273-103">Obtém a configuração de acesso de um locatário.</span><span class="sxs-lookup"><span data-stu-id="5a273-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="5a273-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a273-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a273-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a273-105">DESCRIPTION</span></span>
<span data-ttu-id="5a273-106">O cmdlet **Get-AzApiManagementTenantAccess** obtém a configuração de acesso de locatário para um locatário.</span><span class="sxs-lookup"><span data-stu-id="5a273-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="5a273-107">As teclas não serão incluídas nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="5a273-107">Keys will not be included into result details.</span></span> <span data-ttu-id="5a273-108">Para obter o segredo do cliente, use **Get-AzApiManagementTenantAccessSec limited.**</span><span class="sxs-lookup"><span data-stu-id="5a273-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="5a273-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a273-109">EXAMPLES</span></span>

### <span data-ttu-id="5a273-110">Exemplo 1: Obter configuração de acesso de locatário</span><span class="sxs-lookup"><span data-stu-id="5a273-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="5a273-111">Esse comando obtém a configuração de acesso do locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="5a273-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="5a273-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a273-112">PARAMETERS</span></span>

### <span data-ttu-id="5a273-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5a273-113">-Context</span></span>
<span data-ttu-id="5a273-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="5a273-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5a273-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a273-115">-DefaultProfile</span></span>
<span data-ttu-id="5a273-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5a273-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a273-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a273-117">CommonParameters</span></span>
<span data-ttu-id="5a273-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a273-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a273-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a273-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a273-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="5a273-120">INPUTS</span></span>

### <span data-ttu-id="5a273-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5a273-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="5a273-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="5a273-122">OUTPUTS</span></span>

### <span data-ttu-id="5a273-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="5a273-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="5a273-124">Notas</span><span class="sxs-lookup"><span data-stu-id="5a273-124">NOTES</span></span>

## <span data-ttu-id="5a273-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a273-125">RELATED LINKS</span></span>

[<span data-ttu-id="5a273-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5a273-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


