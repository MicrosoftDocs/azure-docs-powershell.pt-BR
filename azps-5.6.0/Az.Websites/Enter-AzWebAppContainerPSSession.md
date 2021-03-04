---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: e889e3f8d3d94993494c10141629eee6dceed01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887934"
---
# <span data-ttu-id="9b1ad-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="9b1ad-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="9b1ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1ad-103">Abre uma sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9b1ad-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="9b1ad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9b1ad-104">SYNTAX</span></span>

### <span data-ttu-id="9b1ad-105">S1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9b1ad-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b1ad-106">S2</span><span class="sxs-lookup"><span data-stu-id="9b1ad-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b1ad-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9b1ad-107">DESCRIPTION</span></span>
<span data-ttu-id="9b1ad-108">abre uma sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9b1ad-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="9b1ad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b1ad-109">EXAMPLES</span></span>

### <span data-ttu-id="9b1ad-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b1ad-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="9b1ad-111">Este comando abre uma sessão remota do PowerShell no aplicativo de contêiner do Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="9b1ad-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="9b1ad-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9b1ad-112">PARAMETERS</span></span>

### <span data-ttu-id="9b1ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1ad-113">-DefaultProfile</span></span>
<span data-ttu-id="9b1ad-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b1ad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9b1ad-115">-Force</span></span>
<span data-ttu-id="9b1ad-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9b1ad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9b1ad-117">-Name</span></span>
<span data-ttu-id="9b1ad-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1ad-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b1ad-119">-PassThru</span></span>
<span data-ttu-id="9b1ad-120">Retornar um valor que indica sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="9b1ad-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="9b1ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b1ad-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1ad-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="9b1ad-123">-SlotName</span></span>
<span data-ttu-id="9b1ad-124">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1ad-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9b1ad-125">-WebApp</span></span>
<span data-ttu-id="9b1ad-126">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="9b1ad-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1ad-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b1ad-127">-Confirm</span></span>
<span data-ttu-id="9b1ad-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b1ad-129">-WhatIf</span></span>
<span data-ttu-id="9b1ad-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b1ad-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1ad-132">CommonParameters</span></span>
<span data-ttu-id="9b1ad-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1ad-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b1ad-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1ad-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b1ad-135">INPUTS</span></span>

### <span data-ttu-id="9b1ad-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9b1ad-136">System.String</span></span>

### <span data-ttu-id="9b1ad-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9b1ad-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9b1ad-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9b1ad-138">OUTPUTS</span></span>

### <span data-ttu-id="9b1ad-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="9b1ad-139">System.Void</span></span>

## <span data-ttu-id="9b1ad-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="9b1ad-140">NOTES</span></span>

## <span data-ttu-id="9b1ad-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b1ad-141">RELATED LINKS</span></span>
