---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775250"
---
# <span data-ttu-id="45f9c-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="45f9c-101">Get-AzProfile</span></span>

## <span data-ttu-id="45f9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="45f9c-103">Obtenha os perfis de serviço com suporte dos módulos instalados.</span><span class="sxs-lookup"><span data-stu-id="45f9c-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="45f9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45f9c-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="45f9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45f9c-105">DESCRIPTION</span></span>
<span data-ttu-id="45f9c-106">Obtenha os perfis de serviço com suporte dos módulos instalados.</span><span class="sxs-lookup"><span data-stu-id="45f9c-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="45f9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45f9c-107">EXAMPLES</span></span>

### <span data-ttu-id="45f9c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45f9c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="45f9c-109">Obter o perfil de serviço compatível com o módulo do keyvault</span><span class="sxs-lookup"><span data-stu-id="45f9c-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="45f9c-110">OS</span><span class="sxs-lookup"><span data-stu-id="45f9c-110">PARAMETERS</span></span>

### <span data-ttu-id="45f9c-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="45f9c-111">-ListAvailable</span></span>
<span data-ttu-id="45f9c-112">Listar todos os perfis de serviço com suporte pelos módulos instalados</span><span class="sxs-lookup"><span data-stu-id="45f9c-112">List all service profiles supported by installed modules</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45f9c-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="45f9c-113">-ModuleName</span></span>
<span data-ttu-id="45f9c-114">O nome do módulo a ser verificado</span><span class="sxs-lookup"><span data-stu-id="45f9c-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45f9c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f9c-115">CommonParameters</span></span>
<span data-ttu-id="45f9c-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45f9c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f9c-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45f9c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f9c-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45f9c-118">INPUTS</span></span>

### <span data-ttu-id="45f9c-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="45f9c-119">None</span></span>

## <span data-ttu-id="45f9c-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45f9c-120">OUTPUTS</span></span>

### <span data-ttu-id="45f9c-121">Microsoft. Azure. Commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="45f9c-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="45f9c-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45f9c-122">NOTES</span></span>

## <span data-ttu-id="45f9c-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45f9c-123">RELATED LINKS</span></span>
