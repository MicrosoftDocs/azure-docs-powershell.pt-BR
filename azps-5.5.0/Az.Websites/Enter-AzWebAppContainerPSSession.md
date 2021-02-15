---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112341"
---
# <span data-ttu-id="18b65-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="18b65-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="18b65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18b65-102">SYNOPSIS</span></span>
<span data-ttu-id="18b65-103">Abre uma sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="18b65-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="18b65-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18b65-104">SYNTAX</span></span>

### <span data-ttu-id="18b65-105">S1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18b65-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18b65-106">S2</span><span class="sxs-lookup"><span data-stu-id="18b65-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18b65-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="18b65-107">DESCRIPTION</span></span>
<span data-ttu-id="18b65-108">abre uma sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="18b65-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="18b65-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18b65-109">EXAMPLES</span></span>

### <span data-ttu-id="18b65-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18b65-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="18b65-111">Este comando abre uma sessão remota do PowerShell no aplicativo contêiner do Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="18b65-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="18b65-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18b65-112">PARAMETERS</span></span>

### <span data-ttu-id="18b65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b65-113">-DefaultProfile</span></span>
<span data-ttu-id="18b65-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18b65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b65-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="18b65-115">-Force</span></span>
<span data-ttu-id="18b65-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="18b65-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="18b65-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="18b65-117">-Name</span></span>
<span data-ttu-id="18b65-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="18b65-118">The name of the web app.</span></span>

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

### <span data-ttu-id="18b65-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18b65-119">-PassThru</span></span>
<span data-ttu-id="18b65-120">Retornar um valor indicando sucesso ou fracasso</span><span class="sxs-lookup"><span data-stu-id="18b65-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="18b65-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b65-121">-ResourceGroupName</span></span>
<span data-ttu-id="18b65-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="18b65-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="18b65-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="18b65-123">-SlotName</span></span>
<span data-ttu-id="18b65-124">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="18b65-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="18b65-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="18b65-125">-WebApp</span></span>
<span data-ttu-id="18b65-126">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="18b65-126">The web app object</span></span>

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

### <span data-ttu-id="18b65-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="18b65-127">-Confirm</span></span>
<span data-ttu-id="18b65-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18b65-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b65-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b65-129">-WhatIf</span></span>
<span data-ttu-id="18b65-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="18b65-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18b65-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18b65-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b65-132">CommonParameters</span></span>
<span data-ttu-id="18b65-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b65-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b65-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b65-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="18b65-135">INPUTS</span></span>

### <span data-ttu-id="18b65-136">System.String</span><span class="sxs-lookup"><span data-stu-id="18b65-136">System.String</span></span>

### <span data-ttu-id="18b65-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="18b65-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18b65-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="18b65-138">OUTPUTS</span></span>

### <span data-ttu-id="18b65-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="18b65-139">System.Void</span></span>

## <span data-ttu-id="18b65-140">Notas</span><span class="sxs-lookup"><span data-stu-id="18b65-140">NOTES</span></span>

## <span data-ttu-id="18b65-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18b65-141">RELATED LINKS</span></span>
