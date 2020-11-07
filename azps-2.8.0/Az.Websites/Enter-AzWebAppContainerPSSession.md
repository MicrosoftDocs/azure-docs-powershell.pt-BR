---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: b18008268ffd07369cf527c53d6ad693a38d85f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774380"
---
# <span data-ttu-id="758a7-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="758a7-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="758a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="758a7-102">SYNOPSIS</span></span>
<span data-ttu-id="758a7-103">Abre uma sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="758a7-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="758a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="758a7-104">SYNTAX</span></span>

### <span data-ttu-id="758a7-105">S1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="758a7-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758a7-106">S2</span><span class="sxs-lookup"><span data-stu-id="758a7-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="758a7-107">DESCRIPTION</span></span>
<span data-ttu-id="758a7-108">abre uma sessão remota do PowerShell no contêiner do Windows especificado em determinado site ou slot e em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="758a7-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="758a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="758a7-109">EXAMPLES</span></span>

### <span data-ttu-id="758a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="758a7-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="758a7-111">Esse comando abre uma sessão remota do PowerShell no aplicativo contêiner do Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="758a7-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="758a7-112">OS</span><span class="sxs-lookup"><span data-stu-id="758a7-112">PARAMETERS</span></span>

### <span data-ttu-id="758a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758a7-113">-DefaultProfile</span></span>
<span data-ttu-id="758a7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="758a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="758a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="758a7-115">-Force</span></span>
<span data-ttu-id="758a7-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="758a7-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="758a7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="758a7-117">-Name</span></span>
<span data-ttu-id="758a7-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="758a7-118">The name of the web app.</span></span>

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

### <span data-ttu-id="758a7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="758a7-119">-PassThru</span></span>
<span data-ttu-id="758a7-120">Retornar um valor que indica êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="758a7-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="758a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="758a7-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="758a7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="758a7-123">-Slotname</span><span class="sxs-lookup"><span data-stu-id="758a7-123">-SlotName</span></span>
<span data-ttu-id="758a7-124">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="758a7-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="758a7-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="758a7-125">-WebApp</span></span>
<span data-ttu-id="758a7-126">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="758a7-126">The web app object</span></span>

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

### <span data-ttu-id="758a7-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="758a7-127">-Confirm</span></span>
<span data-ttu-id="758a7-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758a7-129">-WhatIf</span></span>
<span data-ttu-id="758a7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="758a7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="758a7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="758a7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758a7-132">CommonParameters</span></span>
<span data-ttu-id="758a7-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758a7-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="758a7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758a7-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="758a7-135">INPUTS</span></span>

### <span data-ttu-id="758a7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="758a7-136">System.String</span></span>

### <span data-ttu-id="758a7-137">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="758a7-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="758a7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="758a7-138">OUTPUTS</span></span>

### <span data-ttu-id="758a7-139">System. void</span><span class="sxs-lookup"><span data-stu-id="758a7-139">System.Void</span></span>

## <span data-ttu-id="758a7-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="758a7-140">NOTES</span></span>

## <span data-ttu-id="758a7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="758a7-141">RELATED LINKS</span></span>