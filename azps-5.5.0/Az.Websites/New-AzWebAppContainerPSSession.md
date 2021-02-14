---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115584"
---
# <span data-ttu-id="61103-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="61103-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="61103-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61103-102">SYNOPSIS</span></span>
<span data-ttu-id="61103-103">New-AzWebAppContainerPSSession criará uma nova Sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="61103-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="61103-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61103-104">SYNTAX</span></span>

### <span data-ttu-id="61103-105">S1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="61103-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61103-106">S2</span><span class="sxs-lookup"><span data-stu-id="61103-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61103-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="61103-107">DESCRIPTION</span></span>
<span data-ttu-id="61103-108">New-AzWebAppContainerPSSession criará uma nova Sessão remota do PowerShell no contêiner do Windows especificado em um determinado site ou slot e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="61103-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="61103-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61103-109">EXAMPLES</span></span>

### <span data-ttu-id="61103-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61103-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="61103-111">Isso criará uma nova Sessão remota do PowerShell no aplicativo contêiner do Windows ContosoASP e mostrará os processos que estão em execução no contêiner ContosoASP</span><span class="sxs-lookup"><span data-stu-id="61103-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="61103-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61103-112">PARAMETERS</span></span>

### <span data-ttu-id="61103-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61103-113">-DefaultProfile</span></span>
<span data-ttu-id="61103-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61103-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61103-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="61103-115">-Force</span></span>
<span data-ttu-id="61103-116">Crie a sessão do PowerShell sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="61103-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="61103-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="61103-117">-Name</span></span>
<span data-ttu-id="61103-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="61103-118">The name of the web app.</span></span>

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

### <span data-ttu-id="61103-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61103-119">-ResourceGroupName</span></span>
<span data-ttu-id="61103-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61103-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="61103-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="61103-121">-SlotName</span></span>
<span data-ttu-id="61103-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="61103-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="61103-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="61103-123">-WebApp</span></span>
<span data-ttu-id="61103-124">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="61103-124">The web app object</span></span>

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

### <span data-ttu-id="61103-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="61103-125">-Confirm</span></span>
<span data-ttu-id="61103-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61103-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61103-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61103-127">-WhatIf</span></span>
<span data-ttu-id="61103-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="61103-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61103-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61103-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61103-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61103-130">CommonParameters</span></span>
<span data-ttu-id="61103-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61103-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61103-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61103-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61103-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="61103-133">INPUTS</span></span>

### <span data-ttu-id="61103-134">System.String</span><span class="sxs-lookup"><span data-stu-id="61103-134">System.String</span></span>

### <span data-ttu-id="61103-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="61103-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="61103-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="61103-136">OUTPUTS</span></span>

### <span data-ttu-id="61103-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="61103-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="61103-138">Notas</span><span class="sxs-lookup"><span data-stu-id="61103-138">NOTES</span></span>

## <span data-ttu-id="61103-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61103-139">RELATED LINKS</span></span>
