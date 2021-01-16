---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260599"
---
# <span data-ttu-id="cc6fd-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="cc6fd-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="cc6fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6fd-103">Abre uma sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cc6fd-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="cc6fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc6fd-104">SYNTAX</span></span>

### <span data-ttu-id="cc6fd-105">S1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc6fd-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc6fd-106">S2</span><span class="sxs-lookup"><span data-stu-id="cc6fd-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc6fd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc6fd-107">DESCRIPTION</span></span>
<span data-ttu-id="cc6fd-108">abre uma sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cc6fd-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="cc6fd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc6fd-109">EXAMPLES</span></span>

### <span data-ttu-id="cc6fd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc6fd-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="cc6fd-111">Esse comando abre uma sessão remota do PowerShell no aplicativo contêiner do Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="cc6fd-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="cc6fd-112">OS</span><span class="sxs-lookup"><span data-stu-id="cc6fd-112">PARAMETERS</span></span>

### <span data-ttu-id="cc6fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6fd-113">-DefaultProfile</span></span>
<span data-ttu-id="cc6fd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc6fd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc6fd-115">-Force</span></span>
<span data-ttu-id="cc6fd-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cc6fd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc6fd-117">-Name</span></span>
<span data-ttu-id="cc6fd-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-118">The name of the web app.</span></span>

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

### <span data-ttu-id="cc6fd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc6fd-119">-PassThru</span></span>
<span data-ttu-id="cc6fd-120">Retornar um valor que indica êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="cc6fd-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="cc6fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc6fd-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc6fd-123">-Slotname</span><span class="sxs-lookup"><span data-stu-id="cc6fd-123">-SlotName</span></span>
<span data-ttu-id="cc6fd-124">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="cc6fd-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cc6fd-125">-WebApp</span></span>
<span data-ttu-id="cc6fd-126">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="cc6fd-126">The web app object</span></span>

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

### <span data-ttu-id="cc6fd-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc6fd-127">-Confirm</span></span>
<span data-ttu-id="cc6fd-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc6fd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc6fd-129">-WhatIf</span></span>
<span data-ttu-id="cc6fd-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc6fd-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc6fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6fd-132">CommonParameters</span></span>
<span data-ttu-id="cc6fd-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6fd-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc6fd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6fd-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc6fd-135">INPUTS</span></span>

### <span data-ttu-id="cc6fd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cc6fd-136">System.String</span></span>

### <span data-ttu-id="cc6fd-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cc6fd-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cc6fd-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc6fd-138">OUTPUTS</span></span>

### <span data-ttu-id="cc6fd-139">System. void</span><span class="sxs-lookup"><span data-stu-id="cc6fd-139">System.Void</span></span>

## <span data-ttu-id="cc6fd-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc6fd-140">NOTES</span></span>

## <span data-ttu-id="cc6fd-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc6fd-141">RELATED LINKS</span></span>
