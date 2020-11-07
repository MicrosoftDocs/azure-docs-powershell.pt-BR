---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942853"
---
# <span data-ttu-id="f5936-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="f5936-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="f5936-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5936-102">SYNOPSIS</span></span>
<span data-ttu-id="f5936-103">Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="f5936-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="f5936-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5936-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5936-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5936-105">DESCRIPTION</span></span>
<span data-ttu-id="f5936-106">O cmdlet **Get-AzApiManagementTenantSyncState** Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="f5936-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="f5936-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5936-107">EXAMPLES</span></span>

### <span data-ttu-id="f5936-108">Exemplo 1: obter o status da sincronização mais recente</span><span class="sxs-lookup"><span data-stu-id="f5936-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="f5936-109">Esse comando obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="f5936-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="f5936-110">OS</span><span class="sxs-lookup"><span data-stu-id="f5936-110">PARAMETERS</span></span>

### <span data-ttu-id="f5936-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f5936-111">-Context</span></span>
<span data-ttu-id="f5936-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f5936-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f5936-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5936-113">-DefaultProfile</span></span>
<span data-ttu-id="f5936-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5936-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5936-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5936-115">CommonParameters</span></span>
<span data-ttu-id="f5936-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5936-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5936-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5936-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5936-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5936-118">INPUTS</span></span>

### <span data-ttu-id="f5936-119">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f5936-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="f5936-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5936-120">OUTPUTS</span></span>

### <span data-ttu-id="f5936-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="f5936-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="f5936-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5936-122">NOTES</span></span>

## <span data-ttu-id="f5936-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5936-123">RELATED LINKS</span></span>
