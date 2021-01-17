---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432692"
---
# <span data-ttu-id="55ee4-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="55ee4-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="55ee4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="55ee4-103">Obtém a configuração de acesso ao git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="55ee4-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="55ee4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55ee4-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55ee4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="55ee4-106">O cmdlet **Get-AzApiManagementTenantGitAccess** Obtém a configuração de acesso ao git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="55ee4-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="55ee4-107">As teclas não serão incluídas nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="55ee4-107">Keys will not be included into result details.</span></span> <span data-ttu-id="55ee4-108">Para obter o segredo do cliente, use **Get-AzApiManagementTenantGitAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="55ee4-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="55ee4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55ee4-109">EXAMPLES</span></span>

### <span data-ttu-id="55ee4-110">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="55ee4-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="55ee4-111">Este comando obtém a configuração de acesso ao git para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="55ee4-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="55ee4-112">OS</span><span class="sxs-lookup"><span data-stu-id="55ee4-112">PARAMETERS</span></span>

### <span data-ttu-id="55ee4-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="55ee4-113">-Context</span></span>
<span data-ttu-id="55ee4-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="55ee4-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="55ee4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ee4-115">-DefaultProfile</span></span>
<span data-ttu-id="55ee4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55ee4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55ee4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ee4-117">CommonParameters</span></span>
<span data-ttu-id="55ee4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ee4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ee4-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55ee4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ee4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55ee4-120">INPUTS</span></span>

### <span data-ttu-id="55ee4-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="55ee4-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="55ee4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55ee4-122">OUTPUTS</span></span>

### <span data-ttu-id="55ee4-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="55ee4-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="55ee4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55ee4-124">NOTES</span></span>

## <span data-ttu-id="55ee4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55ee4-125">RELATED LINKS</span></span>
